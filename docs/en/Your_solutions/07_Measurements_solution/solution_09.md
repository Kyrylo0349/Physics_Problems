# Task 09 – Pendulum Measurements

## Problem Statement

Create a pendulum simulator in HTML with a stopwatch for manual timing. Assume the string length is exact. Perform 10 measurements of the time for 10 complete oscillations and determine:

- the mean period,
- the standard deviation,
- the gravitational acceleration,
- the uncertainty in the result.

## Theory

For a simple pendulum with small oscillations,

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

so

$$
g = \frac{4\pi^2 L}{T^2}
$$

If the length $L$ is treated as exact, then the relative uncertainty is

$$
\frac{\Delta g}{g} \approx 2 \frac{\Delta T}{T}
$$

For each measurement of 10 oscillations,

$$
T_i = \frac{t_i}{10}
$$

The mean period is

$$
\bar{T} = \frac{1}{N}\sum_{i=1}^{N} T_i
$$

The sample standard deviation is

$$
s_T = \sqrt{\frac{1}{N-1}\sum_{i=1}^{N}(T_i-\bar{T})^2}
$$

## Step-by-Step Solution

After timing 10 trials of 10 oscillations each, calculate the periods:

$$
T_i = \frac{t_i}{10}
$$

Then compute

$$
\bar{T} = \frac{1}{10}\sum_{i=1}^{10} T_i
$$

$$
s_T = \sqrt{\frac{1}{9}\sum_{i=1}^{10}(T_i-\bar{T})^2}
$$

Now determine gravity:

$$
g = \frac{4\pi^2 L}{\bar{T}^2}
$$

and the uncertainty:

$$
\Delta g \approx g \cdot 2 \frac{s_T}{\bar{T}}
$$

For a real-life version of the experiment, the same formulas apply after measuring the pendulum length and recording the stopwatch data.

## Final Result

The final experimental result should be reported as

$$
g = g_{\text{calc}} \pm \Delta g
$$

after the measurements are collected.

## Interpretation

Because the period enters as

$$
T^{-2}
$$

even a modest timing uncertainty affects the calculated value of $g$ noticeably.





















<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Pendulum Measurement Simulator</title>
  <style>
    body { font-family: Arial, sans-serif; background:#0f172a; color:#e2e8f0; margin:0; }
    .wrap { max-width:1000px; margin:0 auto; padding:20px; }
    .panel { display:grid; grid-template-columns: 320px 1fr; gap:20px; }
    .card { background:#111827; border:1px solid #334155; border-radius:12px; padding:16px; }
    canvas { background:#020617; border:1px solid #334155; border-radius:12px; }
    button, input { margin-top:8px; }
    table { width:100%; border-collapse:collapse; margin-top:12px; }
    th, td { border:1px solid #334155; padding:6px; text-align:center; }
    .small { color:#cbd5e1; font-size:14px; }
  </style>
</head>
<body>
<div class="wrap">
  <h1>Pendulum Simulator</h1>
  <div class="panel">
    <div class="card">
      <label>Pendulum length L (m)</label>
      <input id="length" type="number" step="0.01" value="1.00">

      <label>Initial angle (degrees)</label>
      <input id="angle" type="number" step="1" value="15">

      <div>
        <button id="startBtn">Start stopwatch</button>
        <button id="stopBtn">Stop stopwatch</button>
        <button id="resetBtn">Reset</button>
        <button id="recordBtn">Record trial</button>
      </div>

      <p>Stopwatch: <span id="time">0.00</span> s</p>
      <p class="small">Measure the time for 10 complete oscillations.</p>

      <table>
        <thead>
          <tr><th>Trial</th><th>Time for 10 osc. (s)</th><th>Period (s)</th></tr>
        </thead>
        <tbody id="tbody"></tbody>
      </table>

      <p>Mean period: <span id="meanT">-</span></p>
      <p>Std. dev.: <span id="stdT">-</span></p>
      <p>Calculated g: <span id="gcalc">-</span></p>
      <p>Uncertainty in g: <span id="dgcalc">-</span></p>
    </div>

    <div class="card">
      <canvas id="canvas" width="600" height="500"></canvas>
    </div>
  </div>
</div>

<script>
const canvas = document.getElementById("canvas");
const ctx = canvas.getContext("2d");
const timeEl = document.getElementById("time");
const tbody = document.getElementById("tbody");
const meanTEl = document.getElementById("meanT");
const stdTEl = document.getElementById("stdT");
const gcalcEl = document.getElementById("gcalc");
const dgcalcEl = document.getElementById("dgcalc");

let running = false;
let watchTime = 0;
let last = performance.now();
let trials = [];
const g0 = 9.81;

function mean(arr) {
  return arr.reduce((a,b) => a+b, 0) / arr.length;
}

function stdSample(arr) {
  if (arr.length < 2) return 0;
  const m = mean(arr);
  const s = arr.reduce((a,b) => a + (b - m) ** 2, 0);
  return Math.sqrt(s / (arr.length - 1));
}

function updateStats() {
  if (trials.length === 0) return;
  const periods = trials.map(t => t / 10);
  const mT = mean(periods);
  const sT = stdSample(periods);
  const L = parseFloat(document.getElementById("length").value);
  const gCalc = 4 * Math.PI * Math.PI * L / (mT * mT);
  const dg = gCalc * 2 * sT / mT;

  meanTEl.textContent = mT.toFixed(4) + " s";
  stdTEl.textContent = sT.toFixed(4) + " s";
  gcalcEl.textContent = gCalc.toFixed(4) + " m/s^2";
  dgcalcEl.textContent = dg.toFixed(4) + " m/s^2";
}

function redrawTable() {
  tbody.innerHTML = "";
  trials.forEach((t, i) => {
    const tr = document.createElement("tr");
    tr.innerHTML = `<td>${i + 1}</td><td>${t.toFixed(2)}</td><td>${(t / 10).toFixed(4)}</td>`;
    tbody.appendChild(tr);
  });
  updateStats();
}

document.getElementById("startBtn").onclick = () => running = true;
document.getElementById("stopBtn").onclick = () => running = false;
document.getElementById("resetBtn").onclick = () => {
  running = false;
  watchTime = 0;
  trials = [];
  timeEl.textContent = "0.00";
  tbody.innerHTML = "";
  meanTEl.textContent = "-";
  stdTEl.textContent = "-";
  gcalcEl.textContent = "-";
  dgcalcEl.textContent = "-";
};
document.getElementById("recordBtn").onclick = () => {
  if (trials.length < 10) {
    trials.push(watchTime);
    redrawTable();
  }
};

function animate(now) {
  const dt = (now - last) / 1000;
  last = now;
  if (running) {
    watchTime += dt;
    timeEl.textContent = watchTime.toFixed(2);
  }

  const L = parseFloat(document.getElementById("length").value);
  const angle0 = parseFloat(document.getElementById("angle").value) * Math.PI / 180;
  const omega = Math.sqrt(g0 / L);
  const t = now / 1000;
  const theta = angle0 * Math.cos(omega * t);

  const originX = 300;
  const originY = 60;
  const scale = 220;
  const bobX = originX + scale * L * Math.sin(theta);
  const bobY = originY + scale * L * Math.cos(theta);

  ctx.clearRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = "#e2e8f0";
  ctx.fillRect(originX - 80, originY - 10, 160, 10);

  ctx.beginPath();
  ctx.moveTo(originX, originY);
  ctx.lineTo(bobX, bobY);
  ctx.strokeStyle = "#94a3b8";
  ctx.lineWidth = 3;
  ctx.stroke();

  ctx.beginPath();
  ctx.arc(bobX, bobY, 20, 0, 2 * Math.PI);
  ctx.fillStyle = "#38bdf8";
  ctx.fill();

  requestAnimationFrame(animate);
}
requestAnimationFrame(animate);
</script>
</body>
</html>
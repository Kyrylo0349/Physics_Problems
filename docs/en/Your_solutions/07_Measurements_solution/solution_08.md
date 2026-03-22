# Task 08 – Mass-Spring Measurements

## Problem Statement

Create a simulator of a mass suspended on a spring in HTML with a timing function. Treat the mass as exact, perform 10 measurements of the time for 10 oscillations, then calculate:

- the mean period,
- the standard deviation,
- the spring constant,
- the uncertainty of the spring constant.

## Theory

For a mass-spring oscillator,

$$
T = 2\pi \sqrt{\frac{m}{k}}
$$

So the spring constant is

$$
k = \frac{4\pi^2 m}{T^2}
$$

If the mass is exact, then the uncertainty in $k$ comes from the uncertainty in the period:

$$
\frac{\Delta k}{k} \approx 2 \frac{\Delta T}{T}
$$

If each measured time corresponds to 10 oscillations, then for each trial

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

Run the HTML simulator and record 10 values of the time for 10 oscillations:

$$
t_1,\ t_2,\ \dots,\ t_{10}
$$

Convert each to a period:

$$
T_i = \frac{t_i}{10}
$$

Then compute:

$$
\bar{T} = \frac{1}{10}\sum_{i=1}^{10} T_i
$$

$$
s_T = \sqrt{\frac{1}{9}\sum_{i=1}^{10}(T_i-\bar{T})^2}
$$

Finally calculate

$$
k = \frac{4\pi^2 m}{\bar{T}^2}
$$

and its uncertainty:

$$
\Delta k \approx k \cdot 2 \frac{s_T}{\bar{T}}
$$

## Final Result

The final reported result should be written in the form

$$
k = k_{\text{calc}} \pm \Delta k
$$

after the measurements are collected.

## Interpretation

A more precise timing measurement gives a smaller uncertainty in the period, which directly improves the precision of the calculated spring constant.



















<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Mass-Spring Measurement Simulator</title>
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
  <h1>Mass-Spring Simulator</h1>
  <div class="panel">
    <div class="card">
      <label>Mass m (kg)</label>
      <input id="mass" type="number" step="0.1" value="1.0">

      <label>Spring constant k (N/m)</label>
      <input id="kval" type="number" step="0.1" value="10.0">

      <div>
        <button id="startBtn">Start stopwatch</button>
        <button id="stopBtn">Stop stopwatch</button>
        <button id="resetBtn">Reset</button>
        <button id="recordBtn">Record trial</button>
      </div>

      <p>Stopwatch: <span id="time">0.00</span> s</p>
      <p class="small">Use the stopwatch to measure the time for 10 full oscillations.</p>

      <table>
        <thead>
          <tr><th>Trial</th><th>Time for 10 osc. (s)</th><th>Period (s)</th></tr>
        </thead>
        <tbody id="tbody"></tbody>
      </table>

      <p>Mean period: <span id="meanT">-</span></p>
      <p>Std. dev.: <span id="stdT">-</span></p>
      <p>Calculated k: <span id="kcalc">-</span></p>
      <p>Uncertainty in k: <span id="dkcalc">-</span></p>
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
const kcalcEl = document.getElementById("kcalc");
const dkcalcEl = document.getElementById("dkcalc");

let running = false;
let watchTime = 0;
let last = performance.now();
let trials = [];

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
  const m = parseFloat(document.getElementById("mass").value);
  const kCalc = 4 * Math.PI * Math.PI * m / (mT * mT);
  const dk = kCalc * 2 * sT / mT;

  meanTEl.textContent = mT.toFixed(4) + " s";
  stdTEl.textContent = sT.toFixed(4) + " s";
  kcalcEl.textContent = kCalc.toFixed(4) + " N/m";
  dkcalcEl.textContent = dk.toFixed(4) + " N/m";
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
  timeEl.textContent = "0.00";
  trials = [];
  tbody.innerHTML = "";
  meanTEl.textContent = "-";
  stdTEl.textContent = "-";
  kcalcEl.textContent = "-";
  dkcalcEl.textContent = "-";
};
document.getElementById("recordBtn").onclick = () => {
  if (trials.length < 10) {
    trials.push(watchTime);
    redrawTable();
  }
};

function drawSpring(x, yTop, yBottom, coils) {
  ctx.beginPath();
  ctx.moveTo(x, yTop);
  const h = (yBottom - yTop) / coils;
  for (let i = 1; i <= coils; i++) {
    const dx = i % 2 === 0 ? -20 : 20;
    ctx.lineTo(x + dx, yTop + i * h);
  }
  ctx.lineTo(x, yBottom);
  ctx.strokeStyle = "#94a3b8";
  ctx.lineWidth = 3;
  ctx.stroke();
}

function animate(now) {
  const dt = (now - last) / 1000;
  last = now;
  if (running) {
    watchTime += dt;
    timeEl.textContent = watchTime.toFixed(2);
  }

  const m = parseFloat(document.getElementById("mass").value);
  const k = parseFloat(document.getElementById("kval").value);
  const omega = Math.sqrt(k / m);
  const t = now / 1000;
  const y = 180 + 80 * Math.cos(omega * t);

  ctx.clearRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = "#e2e8f0";
  ctx.fillRect(220, 40, 160, 10);

  drawSpring(300, 50, y, 16);

  ctx.fillStyle = "#38bdf8";
  ctx.fillRect(255, y, 90, 70);

  ctx.fillStyle = "#e2e8f0";
  ctx.font = "18px Arial";
  ctx.fillText("Mass-spring motion", 220, 470);

  requestAnimationFrame(animate);
}
requestAnimationFrame(animate);
</script>
</body>
</html>
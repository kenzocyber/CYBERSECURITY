<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>PYKCYBER - Hacker Tools</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      background: black;
      color: #00ff00;
      font-family: 'Courier New', monospace;
      overflow: hidden;
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
    }
    .content {
      position: relative;
      z-index: 10;
      padding: 30px;
    }
    h1 {
      font-size: 3em;
      text-align: center;
      margin-bottom: 10px;
    }
    .desc {
      text-align: center;
      font-size: 1.2em;
      margin-bottom: 40px;
      color: #ccc;
    }
    .section {
      margin-bottom: 30px;
    }
    .tools button {
      background: transparent;
      border: 2px solid #00ff00;
      color: #00ff00;
      padding: 10px 20px;
      font-size: 1em;
      margin: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    .tools button:hover {
      background: #00ff00;
      color: black;
      transform: scale(1.1);
    }
    .contact, .footer {
      text-align: center;
    }
    .contact a {
      color: #00ff00;
      text-decoration: none;
    }
    .footer {
      font-size: 0.9em;
      color: #aaa;
      margin-top: 40px;
    }
  </style>
</head>
<body>

<canvas id="cmatrix"></canvas>

<div class="content">
  <h1>PYKCYBER</h1>
  <div class="desc">
    Platform Tools Hacker by Kenzo - <br>
    "Kami tidak hanya menembus sistem. Kami memahami cara kerjanya."
  </div>

  <div class="section">
    <h2>💻 Skill:</h2>
    <ul>
      <li>Python & Bash Scripting</li>
      <li>Ethical Hacking & Recon</li>
      <li>Phishing & Social Engineering</li>
      <li>Termux & Linux Tools</li>
    </ul>
  </div>

  <div class="section tools">
    <h2>🛠️ Tools:</h2>
    <button onclick="alert('Menjalankan Zphisher...')">Zphisher</button>
    <button onclick="alert('Menjalankan Seeker...')">Seeker</button>
    <button onclick="alert('Menjalankan Hydra...')">Hydra Brute Force</button>
    <button onclick="alert('Menjalankan Nmap...')">Nmap Scanner</button>
  </div>

  <div class="section contact">
    <h2>📬 Kontak:</h2>
    <p>📱 WhatsApp: <a href="https://wa.me/6283143490813" target="_blank">0831-4349-0813</a></p>
    <p>✉️ Email: <a href="mailto:Pykcyber@gmail.com">Pykcyber@gmail.com</a></p>
    <p>📸 Instagram: <a href="https://instagram.com/__21chochocaramel" target="_blank">@__21chochocaramel</a></p>
  </div>

  <div class="footer">
    <p>Made by: Kenzo</p>
    <p>Supported by: Berita Payakumbuh</p>
    <p>© 2025 PYKCYBER - Hak cipta dilindungi undang-undang</p>
  </div>
</div>

<script>
// CMatrix Effect
const canvas = document.getElementById("cmatrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

let letters = "01";
letters = letters.split("");

let fontSize = 14;
let columns = canvas.width / fontSize;
let drops = [];
for(let x = 0; x < columns; x++) drops[x] = 1;

function draw() {
  ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = "#0f0";
  ctx.font = fontSize + "px monospace";
  for(let i = 0; i < drops.length; i++) {
    let text = letters[Math.floor(Math.random()*letters.length)];
    ctx.fillText(text, i*fontSize, drops[i]*fontSize);
    if(drops[i]*fontSize > canvas.height && Math.random() > 0.975) drops[i] = 0;
    drops[i]++;
  }
}
setInterval(draw, 33);
</script>

</body>
</html>

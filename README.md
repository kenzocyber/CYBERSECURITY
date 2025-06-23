
<html>
<head>
  <title>PAYAKUMBUH CYBER | PEMIMPIN</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Orbitron', sans-serif;
      background-color: #0a0a0a;
      color: #ffffff;
      overflow: hidden;
      position: relative;
    }

    canvas#cmatrix {
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
      pointer-events: none;
    }

    header {
      padding: 60px 20px;
      text-align: center;
      background: linear-gradient(145deg, #0d0d0d, #1a1a1a);
      box-shadow: 0 0 30px #00ffe0;
      animation: fadeIn 1.5s ease;
    }

    header h1 {
      font-size: 3em;
      color: #00ffe0;
      text-shadow: 0 0 10px #00ffe0, 0 0 20px #00ffe0;
      animation: glow 2s ease-in-out infinite alternate;
    }

    header p {
      margin-top: 10px;
      font-size: 1.1em;
      color: #ccc;
      line-height: 1.8em;
    }

    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
      animation: fadeIn 1.5s ease;
    }

    h2 {
      font-size: 2em;
      color: #00ffe0;
      margin-bottom: 20px;
      border-bottom: 2px solid #00ffe0;
      padding-bottom: 5px;
      text-shadow: 0 0 5px #00ffe0;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .skill-box {
      background-color: #111;
      border: 1px solid #00ffe0;
      padding: 15px;
      text-align: center;
      border-radius: 10px;
      transition: 0.3s;
    }

    .skill-box:hover {
      background-color: #00ffe0;
      color: #000;
      transform: scale(1.05);
    }

    .contact {
      font-size: 1.1em;
      line-height: 2em;
    }

    .contact a {
      color: #00ffe0;
      text-decoration: none;
      text-shadow: 0 0 5px #00ffe0;
    }

    .contact a:hover {
      text-decoration: underline;
    }

    footer {
      background-color: #0d0d0d;
      padding: 30px 20px;
      text-align: center;
      color: #aaa;
      font-size: 0.9em;
      border-top: 1px solid #00ffe0;
      animation: fadeIn 1.5s ease;
    }

    .btn {
      display: inline-block;
      margin: 10px 5px;
      padding: 10px 20px;
      border: 1px solid #00ffe0;
      color: #00ffe0;
      border-radius: 5px;
      transition: 0.3s;
      text-decoration: none;
      text-shadow: 0 0 5px #00ffe0;
    }

    .btn:hover {
      background-color: #00ffe0;
      color: #000;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 5px #00ffe0, 0 0 10px #00ffe0;
      }
      to {
        text-shadow: 0 0 10px #00ffe0, 0 0 20px #00ffe0;
      }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <!-- Matrix Background -->
  <canvas id="cmatrix"></canvas>

  <!-- Header -->
  <header>
    <h1>PAYAKUMBUH CYBER</h1>
    <p>
      Kami adalah unit elit dari Payakumbuh yang menguasai dunia digital. <br>
      Memimpin pergerakan cyber, melacak jejak digital, dan menembus sistem demi edukasi dan keamanan. <br>
      Tidak terlihat, tapi selalu mengawasi. Kami adalah bayangan di jaringan.
    </p>
  </header>

  <!-- Skills Section -->
  <section>
    <h2>Skill Saya</h2>
    <div class="skills-grid">
      <div class="skill-box">Python</div>
      <div class="skill-box">Termux</div>
      <div class="skill-box">Brute Force</div>
      <div class="skill-box">Tracking</div>
      <div class="skill-box">Phishing</div>
      <div class="skill-box">Linux</div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact">
    <h2>Kontak</h2>
    <p>Email: <a href="mailto:pykcyber@gmail.com">pykcyber@gmail.com</a></p>
    <p>HP: <a href="tel:+6283143490913">0831-4349-0913</a></p>
    <p>Instagram: <a href="https://instagram.com/__21chochocaramel" target="_blank">__21chochocaramel</a></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>Made by: <strong>Kenzo</strong></p>
    <p>Supported by: <strong>Berita Payakumbuh</strong></p>
    <p>&copy; 2025 PAYAKUMBUH CYBER. Dilindungi oleh hukum.</p>
  </footer>

  <!-- Matrix Script -->
  <script>
    const canvas = document.getElementById("cmatrix");
    const ctx = canvas.getContext("2d");

    canvas.height = window.innerHeight;
    canvas.width = window.innerWidth;

    const matrix = "01".split("");
    const fontSize = 14;
    const columns = canvas.width / fontSize;
    const drops = Array.from({ length: columns }).fill(1);

    function draw() {
      ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
      ctx.fillRect(0, 0, canvas.width, canvas.height);

      ctx.fillStyle = "#0f0";
      ctx.font = fontSize + "px monospace";

      for (let i = 0; i < drops.length; i++) {
        const text = matrix[Math.floor(Math.random() * matrix.length)];
        ctx.fillText(text, i * fontSize, drops[i] * fontSize);

        if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
          drops[i] = 0;
        }

        drops[i]++;
      }
    }

    setInterval(draw, 33);
  </script>
</body>
</html>

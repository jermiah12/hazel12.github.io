<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hazel Project</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      overflow: hidden;
      display: grid;
      place-items: center;
      background: #000;
      font-family: Arial, Helvetica, sans-serif;
    }

    .love-scene {
      position: relative;
      width: min(94vmin, 720px);
      aspect-ratio: 1;
      display: grid;
      place-items: center;
    }

    .center-image {
      position: relative;
      display: block;
      width: clamp(180px, 33vmin, 290px);
      aspect-ratio: 1;
      object-fit: cover;
      border: 8px solid rgba(255, 255, 255, 0.88);
      border-radius: 50%;
      box-shadow:
        0 24px 70px rgba(255, 0, 80, 0.22),
        0 0 56px rgba(255, 49, 125, 0.72);
      z-index: 5;
      animation: photoPulse 3s ease-in-out infinite;
    }

    .heart-canvas {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      pointer-events: none;
    }

    @keyframes photoPulse {
      0%,
      100% {
        transform: scale(1);
      }

      50% {
        transform: scale(1.035);
      }
    }
  </style>
</head>

<body>
  <main class="love-scene" aria-label="Animated love scene">
    <canvas class="heart-canvas" id="heartCanvas" aria-hidden="true"></canvas>
    <img class="center-image" src="images/bg.JPG" alt="Hazel">
  </main>

  <script>
    const canvas = document.getElementById("heartCanvas");
    const ctx = canvas.getContext("2d");
    const totalWords = 500;
    const word = "ILOVEYOU";
    let words = [];
    let sceneSize = 0;
    let lastFrame = 0;

    if (ctx) {
      resizeCanvas();
      window.addEventListener("resize", resizeCanvas);
      requestAnimationFrame(drawHeartText);
    }

    function resizeCanvas() {
      const rect = canvas.getBoundingClientRect();
      const ratio = Math.min(window.devicePixelRatio || 1, 1.5);

      canvas.width = Math.floor(rect.width * ratio);
      canvas.height = Math.floor(rect.height * ratio);
      ctx.setTransform(ratio, 0, 0, ratio, 0, 0);
      sceneSize = Math.min(rect.width, rect.height);
      words = createHeartWords();
    }

    function createHeartWords() {
      const created = [];
      const centerX = canvas.clientWidth / 2;
      const centerY = canvas.clientHeight * 0.48;
      const scale = sceneSize / 35;
      const rings = 5;
      const wordsPerRing = Math.ceil(totalWords / rings);

      for (let ring = 0; ring < rings; ring++) {
        const ringOffset = ring - (rings - 1) / 2;
        const ringScale = 1 + ringOffset * 0.022;

        for (let i = 0; i < wordsPerRing && created.length < totalWords; i++) {
          const t = (i / wordsPerRing) * Math.PI * 2 + ring * 0.012;
          const point = getHeartPoint(t);

          created.push({
            x: centerX + point.x * scale * ringScale,
            y: centerY - point.y * scale * ringScale + ringOffset * sceneSize * 0.005,
            size: Math.max(5, sceneSize * 0.009 + (ring % 2) * 1.4),
            alpha: 0.58 + (ring % 3) * 0.12,
            delay: (i % 24) * 0.12 + ring * 0.25
          });
        }
      }

      return created;
    }

    function getHeartPoint(t) {
      return {
        x: 16 * Math.pow(Math.sin(t), 3),
        y: 13 * Math.cos(t) - 5 * Math.cos(2 * t) - 2 * Math.cos(3 * t) - Math.cos(4 * t)
      };
    }

    function drawHeartText(time) {
      requestAnimationFrame(drawHeartText);

      if (time - lastFrame < 33) {
        return;
      }

      lastFrame = time;
      const seconds = time / 1000;
      const moveRight = Math.sin(seconds * 1.35) * 12;

      ctx.clearRect(0, 0, canvas.clientWidth, canvas.clientHeight);
      ctx.textAlign = "center";
      ctx.textBaseline = "middle";

      for (const item of words) {
        const pulse = (Math.sin(seconds * 2.2 + item.delay) + 1) / 2;
        const red = Math.round(150 + pulse * 105);
        const pink = Math.round(80 - pulse * 55);

        ctx.font = `900 ${item.size}px Arial, Helvetica, sans-serif`;
        ctx.shadowColor = `rgba(255, ${pink}, ${120 + pulse * 80}, 0.95)`;
        ctx.shadowBlur = 5 + pulse * 8;
        ctx.fillStyle = `rgba(${red}, ${pink}, ${120 + pulse * 70}, ${item.alpha})`;
        ctx.fillText(word, item.x + moveRight, item.y);
      }
    }
  </script>
</body>

</html>

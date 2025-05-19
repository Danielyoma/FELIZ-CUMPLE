<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Feliz Cumpleaños Yuli</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe Script', cursive;
      background: linear-gradient(270deg, #ff9a9e, #fad0c4, #ffd1ff);
      background-size: 600% 600%;
      animation: fondo 20s ease infinite;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      color: #fff;
    }

    @keyframes fondo {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    .mensaje {
      text-align: center;
      font-size: 3em;
      padding: 20px;
      background-color: rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
      backdrop-filter: blur(5px);
      animation: aparecer 2s ease-in-out;
    }

    @keyframes aparecer {
      from {
        transform: scale(0.7);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    .btn {
      margin-top: 30px;
      font-size: 1.2em;
      padding: 12px 24px;
      border: none;
      border-radius: 30px;
      background-color: #ff6f91;
      color: white;
      cursor: pointer;
      transition: background 0.3s;
    }

    .btn:hover {
      background-color: #ff3e6c;
    }

    .oculto {
      display: none;
      margin-top: 20px;
      font-size: 1.5em;
      color: #fff5f5;
      animation: fadeIn 2s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .flotante {
      position: absolute;
      font-size: 2em;
      animation: flotar 5s linear infinite;
    }

    @keyframes flotar {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-100vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="mensaje">
    🎉 ¡Feliz Cumpleaños, Yuli! 🎂<br>
    Eres fuerte, talentosa y capaz. ¡Vas a lograr todas tus metas! ✨
  </div>

  <button class="btn" onclick="mostrarMensaje()">💌 Ver mensaje especial</button>
  <div id="mensajeExtra" class="oculto">
    No hay sueño demasiado grande ni meta imposible para ti.<br>
    ¡Confía en ti y sigue adelante con determinación! 💪🌟
  </div>

  <script>
    function mostrarMensaje() {
      document.getElementById('mensajeExtra').style.display = 'block';
    }

    const elementos = ['🎈', '⭐', '🐱']; // Globos, estrellas y gatitos
    for (let i = 0; i < 50; i++) {
      let flotante = document.createElement('div');
      flotante.classList.add('flotante');
      flotante.innerHTML = elementos[Math.floor(Math.random() * elementos.length)];
      flotante.style.left = Math.random() * 100 + 'vw';
      flotante.style.top = Math.random() * 100 + 'vh';
      flotante.style.animationDuration = (5 + Math.random() * 5) + 's';
      document.body.appendChild(flotante);
    }
  </script>
</body>
</html>

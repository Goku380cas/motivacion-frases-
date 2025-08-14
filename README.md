<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Frases Motivadoras</title>
  <style>
    body {
      background: linear-gradient(to right, #a1c4fd, #c2e9fb);
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      text-align: center;
      color: #333;
    }
    .container {
      background-color: rgba(255, 255, 255, 0.8);
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
      max-width: 600px;
    }
    h1 {
      font-size: 2em;
      margin-bottom: 20px;
      color: #0077b6;
    }
    #frase {
      font-size: 1.5em;
      font-style: italic;
      transition: opacity 0.5s ease;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Bienvenido,🌟</h1>
    <div id="frase">Cargando frase motivadora...</div>
  </div>

  <script>
    const frases = [
      "Cree en ti y todo será posible.",
      "Cada día es una nueva oportunidad para brillar.",
      "Tu actitud determina tu altitud.",
      "No esperes el momento perfecto, haz que el momento sea perfecto.",
      "Eres más fuerte de lo que crees.",
      "La constancia vence lo que la dicha no alcanza.",
      "Hazlo con pasión o no lo hagas.",
      "El éxito es la suma de pequeños esfuerzos repetidos cada día.",
      "Nunca es tarde para empezar de nuevo.",
      "Lo que hoy parece difícil, mañana será tu orgullo."
    ];

    const fraseElemento = document.getElementById("frase");

    function mostrarFrase() {
      const fraseAleatoria = frases[Math.floor(Math.random() * frases.length)];
      fraseElemento.style.opacity = 0;
      setTimeout(() => {
        fraseElemento.textContent = fraseAleatoria;
        fraseElemento.style.opacity = 1;
      }, 500);
    }

    mostrarFrase();
    setInterval(mostrarFrase, 5000); // Cambia cada 5 segundos
  </script>

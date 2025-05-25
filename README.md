[Uplo<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>¿Cuánto me amas?</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      background: #000;
      color: #f0f;
      font-family: 'Courier New', monospace;
      text-align: center;
      padding: 20px;
    }

    h1 {
      color: #ff69b4;
    }

    .pregunta {
      margin: 20px 0;
    }

    input {
      padding: 10px;
      border-radius: 5px;
      border: none;
      font-size: 16px;
      width: 80%;
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 18px;
      background-color: #f0f;
      color: #000;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #ff99ff;
    }

    #resultado {
      margin-top: 30px;
      font-size: 22px;
      color: #0f0;
    }
  </style>
</head>
<body>
  <h1>💖 ¿Cuánto me amas? 💖</h1>
  <p>Responde estas preguntas sobre nosotros...</p>

  <div class="pregunta"><p>1. ¿Cómo me dices de cariño?</p><input type="text" id="p1"></div>
  <div class="pregunta"><p>2. ¿Cuál fue nuestra primera cita?</p><input type="text" id="p2"></div>
  <div class="pregunta"><p>3. ¿Mi color favorito?</p><input type="text" id="p3"></div>
  <div class="pregunta"><p>4. ¿Qué día es nuestro aniversario?</p><input type="text" id="p4"></div>
  <div class="pregunta"><p>5. ¿Qué tanto me quieres?</p><input type="text" id="p5"></div>
  <div class="pregunta"><p>6. ¿te casarias conmigo?</p><input type="text" id="p6"></div>

  <button onclick="evaluar()">Enviar</button>

  <div id="resultado"></div>

  <script>
    function evaluar() {
      const respuestas = {
        p1: "amor",         // puedes cambiar estas respuestas
        p2: "parque",
        p3: "negro",
        p4: "25 de agosto",
        p5: "te amo mucho",
        p6: "si"
      };

      let aciertos = 0;
      for (let i = 1; i <= 6; i++) {
        let user = document.getElementById(`p`).value.trim().toLowerCase();
        if (user === respuestas[`p`]) aciertos++;
      }

      const resultado = document.getElementById("resultado");

      if (aciertos === 6) {
        resultado.innerHTML = "💯 ¡Wow! Me conoces perfectamente... ❤️ ¡TE AMO INFINITO!";
      } else if (aciertos >= 4) {
        resultado.innerHTML = `😊 Muy bien, acertaste /6. ¡Se nota cuánto me amas! 💕`;
      } else if (aciertos >= 2) {
        resultado.innerHTML = `😅 Acertaste /6... ¡Pero sé que tu amor es real! 💗`;
      } else {
        resultado.innerHTML = `🙈 Solo /6... ¡Pero yo te amo igual, aunque estés distraíd@! 😘`;
      }
    }
  </script>
</body>
</html>ading cuanto me amas.html…]()

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Organización 311</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap" rel="stylesheet">
  <style>
    body, html {
      margin: 0;
      padding: 0;
      background-color: #000;
      color: white;
      font-family: 'Poppins', sans-serif;
      height: 100vh;
      overflow: hidden;
    }

    #intro {
      background-color: #000;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0; left: 0;
      z-index: 10;
    }

    #contenido {
      opacity: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      transition: opacity 2s ease;
    }

    h1 {
      font-size: 80px;
      opacity: 0.7;
      margin: 0;
    }

    hr {
      width: 60%;
      border: 1px solid #666;
      margin: 30px auto;
    }

    .mensaje {
      max-width: 700px;
      font-size: 18px;
      line-height: 1.6;
      padding: 0 20px;
    }

    .firma {
      position: absolute;
      bottom: 40px;
      right: 40px;
      font-size: 14px;
      color: #aaa;
      max-width: 250px;
      text-align: right;
    }
  </style>
</head>
<body>
  <div id="intro"></div>

  <div id="contenido">
    <h1>Hola!</h1>
    <hr>
    <div class="mensaje">
      Has sido seleccionad@ para ser comandante de nuestra organización.<br><br>
      Para más información visita al cadete <strong>Rommel Reyes M.</strong> en el <strong>Colegio Militarizado Moderno Alarid</strong>.<br><br>
      No compartas esta información a nadie más, hay consecuencias no tan severas.<br><br>
      Por lo pronto, gracias.
    </div>

    <div class="firma">
      Atentamente,<br>
      <strong>El fundador 311.</strong><br>
      (Puede que sepas mi identidad, pero no la compartas a nadie, por favor.)
    </div>
  </div>

  <!-- Reemplaza el enlace de audio con el fragmento exacto que contiene "BURNOUT!" -->
  <audio id="burn" src="burn-boywithuke.mp3"></audio>

  <script>
    const intro = document.getElementById("intro");
    const contenido = document.getElementById("contenido");
    const audio = document.getElementById("burn");

    // Mostrar pantalla negra por 3 segundos
    setTimeout(() => {
      audio.play().catch(e => console.log("Audio bloqueado por el navegador:", e));

      // Esperar 5.5 segundos para que llegue el "BURNOUT!" (ajústalo si es necesario)
      setTimeout(() => {
        intro.style.display = "none";
        contenido.style.opacity = 1;
      }, 5500); // milisegundos hasta el grito "BURNOUT!"
    }, 3000);
  </script>
</body>
</html>

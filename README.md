<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rosa Animada</title>
<style>
  body {
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #87CEEB; /* Color del cielo */
  }
  #pasto {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 150px;
    background-color: #00FF00; /* Color del pasto */
    z-index: 1;
    overflow: hidden;
  }
  #flor {
    position: absolute;
    bottom: -100px;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    border: 50px solid transparent;
    border-bottom-color: #FFC0CB; /* Color de la rosa */
    z-index: 2;
    animation: crecer 3s forwards, soltar 2s 3s forwards;
  }
  @keyframes crecer {
    0% {
      width: 0;
      height: 0;
      bottom: -100px;
    }
    100% {
      width: 200px;
      height: 200px;
      bottom: 50px;
    }
  }
  @keyframes soltar {
    0% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  }
  #texto {
    position: absolute;
    bottom: 200px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 50px;
    color: #FFC0CB; /* Color del texto */
    opacity: 0;
    animation: aparecer 1s 5s forwards;
  }
  @keyframes aparecer {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
</style>
</head>
<body>
<div id="pasto"></div>
<div id="flor"></div>
<div id="texto">Samira</div>
</body>
</html>

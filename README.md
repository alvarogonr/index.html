<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Una pregunta especial</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600&display=swap" rel="stylesheet">

<style>
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  font-family: 'Montserrat', sans-serif;
  background: linear-gradient(180deg, #e6f6f8, #ffffff);
  overflow: hidden;
}

.slide {
  display: none;
  width: 100%;
  height: 100%;
  padding: 60px;
  box-sizing: border-box;
  text-align: center;
  color: #0b3c49;
  position: relative;
}

.slide.active {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.wave {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 120px;
  background: linear-gradient(to top, rgba(0,180,200,0.15), transparent);
}

.text {
  font-size: 32px;
  line-height: 1.4;
  max-width: 900px;
}

.buttons {
  margin-top: 40px;
  display: flex;
  gap: 24px;
}

button {
  padding: 14px 36px;
  font-size: 18px;
  border-radius: 40px;
  border: none;
  cursor: pointer;
  font-family: 'Montserrat', sans-serif;
  transition: all 0.3s ease;
}

.yes {
  background-color: #1fbac0;
  color: white;
}

.yes:hover {
  background-color: #159aa0;
}

.no {
  background-color: transparent;
  border: 2px solid #1fbac0;
  color: #1fbac0;
}

.no:hover {
  background-color: rgba(31,186,192,0.1);
}

.final-buttons button {
  font-size: 22px;
  padding: 18px 50px;
}

.light {
  position: absolute;
  top: -50px;
  right: -50px;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(255,255,255,0.6), transparent 70%);
}
</style>
</head>

<body>

<div class="slide active">
  <div class="light"></div>
  <div class="text">¿Te gustaría saber por qué te envío esto?</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text">Seguro te preguntas por qué hoy y de esta manera tan especial…<br>¿Quieres descubrirlo?</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text">Ya sabes que yo y las formalidades…<br>no somos mejores amigos.<br>¿Verdad que sí?</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text">Pero también sé que para ti las cosas importantes…<br>¡son importantes!<br>Y eso lo hace especial para mí también.</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text">Hoy la distancia nos jugó una broma,<br>pero no va a impedir esto:<br>¿Te animas a saber qué es?</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text">Porque la lámina 7 será<br>(redoble de tambores…)<br>el día 7,<br>justo un mes después de volver a vernos<br>en ese concierto.</div>
  <div class="buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="no">No</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text" style="font-size:40px;">¿Te gustaría que seamos pareja?</div>
  <div class="buttons final-buttons">
    <button class="yes" onclick="next()">Sí</button>
    <button class="yes" onclick="next()">Sí 😊</button>
  </div>
  <div class="wave"></div>
</div>

<div class="slide">
  <div class="text" style="font-size:38px;">¡gracias por aceptar!<br>nos vemos pronto para celebrar</div>
  <div class="wave"></div>
</div>

<script>
let current = 0;
const slides = document.querySelectorAll('.slide');

function next() {
  slides[current].classList.remove('active');
  current++;
  if (current < slides.length) {
    slides[current].classList.add('active');
  }
}
</script>

</body>
</html>

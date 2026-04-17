<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Recursero — El tiempo es una decisión · Human Experience</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg:      #f7f5f0;
  --white:   #ffffff;
  --black:   #0d0d0d;
  --mid:     #6b6660;
  --faint:   #b8b3ac;
  --line:    rgba(13,13,13,0.12);
  --line2:   rgba(13,13,13,0.22);
  --aa:      #8b7355;   /* cálido / arte */
  --ab:      #4a7c6e;   /* frío / ciencia */
  --ac:      #6b5f7a;   /* síntesis */
  --ad:      #8b4a3a;   /* acción */
}

html, body {
  width: 100%; height: 100%;
  background: var(--bg);
  color: var(--black);
  font-family: 'DM Mono', monospace;
  overflow: hidden;
}

/* ── SLIDES ── */
#slides { position: fixed; inset: 0; z-index: 1; }

.slide {
  position: absolute; inset: 0;
  display: flex; flex-direction: column;
  padding: 3.5rem 5.5rem 5.5rem;
  opacity: 0; transform: translateX(56px);
  transition: opacity .5s cubic-bezier(.4,0,.2,1), transform .5s cubic-bezier(.4,0,.2,1);
  pointer-events: none;
}
.slide.active  { opacity: 1; transform: translateX(0); pointer-events: all; }
.slide.exit    { opacity: 0; transform: translateX(-56px); }

/* ── HEADER ── */
.sh {
  display: flex; align-items: baseline; gap: 1.5rem;
  margin-bottom: 2rem; padding-bottom: 1rem;
  border-bottom: 1px solid var(--line);
  flex-shrink: 0;
}
.sh-num   { font-size: .58rem; letter-spacing: .22em; color: var(--faint); }
.sh-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(1.4rem, 2.6vw, 2.1rem);
  font-weight: 300; font-style: italic;
  color: var(--black); letter-spacing: -.01em;
}
.sh-desc {
  font-size: .62rem; color: var(--mid);
  margin-left: auto; max-width: 36ch;
  text-align: right; line-height: 1.75;
}

/* ── GRID ── */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: .75rem; flex: 1; overflow-y: auto;
  padding-right: .25rem; min-height: 0;
}
.grid::-webkit-scrollbar { width: 2px; }
.grid::-webkit-scrollbar-thumb { background: var(--line2); }
.grid.cols3 { grid-template-columns: repeat(3, 1fr); }

/* ── CARD ── */
.card {
  background: var(--white);
  border: 1px solid var(--line);
  border-radius: 2px;
  padding: .95rem 1.1rem;
  text-decoration: none; color: inherit;
  display: flex; flex-direction: column; gap: .4rem;
  transition: border-color .18s, transform .18s, box-shadow .18s;
  cursor: pointer; position: relative; overflow: hidden;
}
.card::before {
  content: ''; position: absolute;
  top: 0; left: 0; right: 0; height: 2px;
  opacity: 0; transition: opacity .2s;
}
.card:hover { border-color: var(--line2); transform: translateY(-1px); box-shadow: 0 4px 16px rgba(0,0,0,.06); }
.card:hover::before { opacity: 1; }
.card.gen::before { background: var(--aa); }
.card.cap::before { background: var(--ab); }
.card.cod::before { background: var(--ac); }
.card.dat::before { background: var(--ab); }
.card.tip::before { background: var(--aa); }
.card.wide { grid-column: span 2; }

.card-head { display: flex; align-items: center; justify-content: space-between; }
.card-name { font-size: .77rem; font-weight: 400; color: var(--black); letter-spacing: .01em; }
.card-arrow { font-size: .6rem; color: var(--faint); transition: color .18s, transform .18s; }
.card:hover .card-arrow { color: var(--ab); transform: translate(2px,-2px); }
.card-desc { font-size: .65rem; color: var(--mid); line-height: 1.7; }

.card-prompt {
  background: rgba(74,124,110,.05);
  border: 1px solid rgba(74,124,110,.15);
  border-radius: 1px; padding: .4rem .6rem; margin-top: .1rem;
}
.card-prompt-label {
  font-size: .52rem; letter-spacing: .15em; text-transform: uppercase;
  color: rgba(74,124,110,.6); margin-bottom: .2rem;
}
.card-prompt-text { font-size: .6rem; color: rgba(13,13,13,.4); line-height: 1.65; font-style: italic; }
.card.tip .card-prompt { background: rgba(139,115,85,.05); border-color: rgba(139,115,85,.15); }
.card.tip .card-prompt-label { color: rgba(139,115,85,.6); }

.card-tag {
  font-size: .54rem; letter-spacing: .12em; text-transform: uppercase;
  padding: .1rem .45rem; border-radius: 99px; display: inline-block;
  align-self: flex-start; margin-top: auto; padding-top: .35rem;
}
.card.gen .card-tag { background: rgba(139,115,85,.08); color: var(--aa); }
.card.cap .card-tag { background: rgba(74,124,110,.08); color: var(--ab); }
.card.cod .card-tag { background: rgba(107,95,122,.08); color: var(--ac); }
.card.dat .card-tag { background: rgba(74,124,110,.08); color: var(--ab); }

/* ── LANG CARD ── */
.lang-card {
  background: var(--white); border: 1px solid var(--line);
  border-radius: 2px; padding: 1.1rem 1.2rem;
  display: flex; flex-direction: column; gap: .6rem;
  position: relative; overflow: hidden;
}
.lang-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0;
  height: 2px; background: var(--ad); opacity: .5;
}
.lang-name { font-size: .82rem; font-weight: 400; color: var(--black); }
.lang-use  { font-size: .62rem; color: var(--mid); line-height: 1.65; }
.lang-links { display: flex; gap: .45rem; flex-wrap: wrap; }
.lang-link {
  font-size: .58rem; color: var(--ad); text-decoration: none;
  border: 1px solid rgba(139,74,58,.2); border-radius: 99px;
  padding: .15rem .5rem; transition: background .15s;
}
.lang-link:hover { background: rgba(139,74,58,.08); }

/* ── PORTADA ── */
#slide-0 { justify-content: center; }
.p-eyebrow {
  font-size: .6rem; letter-spacing: .25em; text-transform: uppercase;
  color: var(--mid); margin-bottom: 1.5rem;
  display: flex; align-items: center; gap: 1rem;
}
.p-eyebrow::after { content: ''; flex: 1; max-width: 60px; height: 1px; background: var(--line2); }
.p-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(3.5rem, 7vw, 6.5rem);
  font-weight: 300; font-style: italic;
  line-height: 1.0; letter-spacing: -.02em;
  color: var(--black); margin-bottom: .75rem;
}
.p-title em { color: var(--aa); font-style: inherit; }
.p-sub {
  font-size: .7rem; color: var(--mid); line-height: 1.95;
  max-width: 52ch; margin-bottom: 2.5rem;
  border-left: 2px solid var(--line2); padding-left: 1rem;
}
.flow {
  display: flex; align-items: center; gap: .65rem;
  margin-bottom: 2.5rem; flex-wrap: wrap;
}
.flow-step {
  font-size: .58rem; letter-spacing: .12em; text-transform: uppercase;
  padding: .28rem .65rem; border: 1px solid var(--line); border-radius: 99px; color: var(--mid);
}
.flow-step.s1 { border-color: rgba(139,115,85,.4); color: var(--aa); }
.flow-step.s2 { border-color: rgba(74,124,110,.4); color: var(--ab); }
.flow-step.s3 { border-color: rgba(107,95,122,.4); color: var(--ac); }
.flow-arrow { font-size: .55rem; color: var(--faint); }
.p-chips { display: flex; gap: .5rem; flex-wrap: wrap; }
.chip {
  font-size: .58rem; letter-spacing: .12em; text-transform: uppercase;
  padding: .25rem .7rem; border-radius: 99px;
  border: 1px solid var(--line); color: var(--mid);
}
.chip.a { border-color: rgba(139,115,85,.35); color: var(--aa); }
.chip.b { border-color: rgba(74,124,110,.35); color: var(--ab); }
.chip.c { border-color: rgba(107,95,122,.35); color: var(--ac); }
.p-hint {
  position: absolute; bottom: 5rem; right: 5.5rem;
  font-size: .58rem; color: var(--faint); text-align: right; line-height: 1.9;
}
.p-brand {
  position: absolute; top: 3.5rem; right: 5.5rem;
  font-size: .58rem; letter-spacing: .18em; text-transform: uppercase;
  color: var(--faint);
}

/* ── GLOSARIO ── */
.glosario-wrap {
  display: grid; grid-template-columns: 1fr 1.5fr;
  gap: 1.5rem; flex: 1; min-height: 0; overflow: hidden;
}
.glosario-left { display: flex; flex-direction: column; gap: .5rem; min-height: 0; }
.glosario-list {
  display: flex; flex-direction: column; gap: .35rem;
  overflow-y: auto; flex: 1; padding-right: .35rem; min-height: 0;
}
.glosario-list::-webkit-scrollbar { width: 2px; }
.glosario-list::-webkit-scrollbar-thumb { background: var(--line2); }

.glosario-term-btn {
  background: var(--white); border: 1px solid var(--line);
  border-radius: 2px; padding: .48rem .85rem; text-align: left;
  cursor: pointer; font-family: 'DM Mono', monospace;
  font-size: .68rem; color: var(--mid);
  transition: background .15s, border-color .15s, color .15s;
  display: flex; align-items: center; justify-content: space-between; gap: .5rem;
  flex-shrink: 0;
}
.glosario-term-btn:hover { background: var(--bg); border-color: var(--line2); color: var(--black); }
.glosario-term-btn.active { background: rgba(74,124,110,.06); border-color: rgba(74,124,110,.3); color: var(--ab); }
.glosario-term-btn.nuevo { border-color: rgba(107,95,122,.3); color: var(--ac); }
.glosario-term-btn.nuevo.active { background: rgba(107,95,122,.06); }

.glosario-add { border-top: 1px solid var(--line); padding-top: .7rem; flex-shrink: 0; }
.glosario-add-label { font-size: .54rem; letter-spacing: .15em; text-transform: uppercase; color: var(--faint); margin-bottom: .45rem; }
.glosario-add-row { display: flex; gap: .45rem; }
.glosario-add-row input {
  flex: 1; background: var(--white); border: 1px solid var(--line2);
  border-radius: 2px; padding: .4rem .65rem;
  font-family: 'DM Mono', monospace; font-size: .65rem;
  color: var(--black); outline: none; transition: border-color .15s;
}
.glosario-add-row input:focus { border-color: rgba(74,124,110,.5); }
.glosario-add-row input::placeholder { color: var(--faint); }
.glosario-add-row button {
  background: none; border: 1px solid rgba(74,124,110,.3);
  border-radius: 2px; padding: .4rem .85rem;
  font-family: 'DM Mono', monospace; font-size: .65rem;
  color: var(--ab); cursor: pointer; transition: background .15s;
  white-space: nowrap;
}
.glosario-add-row button:hover { background: rgba(74,124,110,.06); }
.glosario-add-row button:disabled { opacity: .4; cursor: default; }
.glosario-status { font-size: .58rem; color: var(--faint); margin-top: .35rem; min-height: .9rem; font-style: italic; }

.glosario-panel {
  background: var(--white); border: 1px solid var(--line);
  border-radius: 2px; padding: 2rem 2.25rem;
  display: flex; flex-direction: column; justify-content: center; gap: .9rem;
  min-height: 0; overflow-y: auto;
}
.glosario-panel-hint { font-size: .65rem; color: var(--faint); font-style: italic; }
.glosario-panel-name {
  font-family: 'Cormorant Garamond', serif;
  font-style: italic; font-size: 1.75rem; font-weight: 300;
  color: var(--black); display: none;
}
.glosario-panel-def { font-size: .7rem; color: var(--mid); line-height: 1.85; display: none; }
.glosario-panel-ej {
  font-size: .65rem; color: var(--faint); line-height: 1.75;
  border-left: 2px solid var(--line2); padding-left: .75rem; display: none;
}

/* ── NAV ── */
#nav {
  position: fixed; bottom: 2rem; left: 50%; transform: translateX(-50%);
  z-index: 10; display: flex; align-items: center; gap: .65rem;
  background: rgba(247,245,240,.9); backdrop-filter: blur(8px);
  border: 1px solid var(--line2); border-radius: 99px;
  padding: .55rem 1.1rem;
}
.nav-dot {
  width: 5px; height: 5px; border-radius: 50%;
  background: var(--faint); cursor: pointer; border: none;
  transition: background .2s, transform .2s;
}
.nav-dot.active { background: var(--black); transform: scale(1.5); }
.nav-sep { width: 1px; height: 12px; background: var(--line); margin: 0 .2rem; }
.nav-btn {
  background: none; border: none; color: var(--mid);
  font-family: 'DM Mono', monospace; font-size: .6rem;
  cursor: pointer; padding: .1rem .35rem; transition: color .15s;
}
.nav-btn:hover { color: var(--black); }
#slide-counter { font-size: .57rem; color: var(--faint); letter-spacing: .1em; min-width: 3ch; text-align: center; }
</style>
</head>
<body>
<div id="slides">

<!-- 0: PORTADA -->
<div class="slide active" id="slide-0">
  <span class="p-brand">Human Experience · Hackathon 2025</span>
  <p class="p-eyebrow">Clínica de Arte Contemporáneo — recursero</p>
  <h1 class="p-title">el tiempo<br>es una <em>decisión</em></h1>
  <p class="p-sub">
    Un sistema audiovisual que se modifica cuando los cuerpos de origami<br>
    se encuentran sobre la mesa. Lo que ese encuentro hace al tiempo,<br>
    lo decidís vos.
  </p>
  <div class="flow">
    <span class="flow-step s1">01 generar</span>
    <span class="flow-arrow">→</span>
    <span class="flow-step s2">02 capturar</span>
    <span class="flow-arrow">→</span>
    <span class="flow-step s2">03 detectar</span>
    <span class="flow-arrow">→</span>
    <span class="flow-step s3">04 conectar</span>
  </div>
  <div class="p-chips">
    <span class="chip a">ia generativa</span>
    <span class="chip b">visión computacional</span>
    <span class="chip c">síntesis &amp; proyección</span>
    <span class="chip">lenguajes</span>
    <span class="chip b">datasets</span>
    <span class="chip">glosario</span>
    <span class="chip">consejos</span>
  </div>
  <p class="p-hint">← → teclado · clic en tarjetas para abrir recursos</p>
</div>

<!-- 1: GENERAR -->
<div class="slide" id="slide-1">
  <div class="sh">
    <span class="sh-num">01</span>
    <h2 class="sh-title">Generar — el material audiovisual</h2>
    <span class="sh-desc">Creá el contenido que vas a proyectar y alterar.<br>Imagen, video, audio generado o encontrado.</span>
  </div>
  <div class="grid">
    <a class="card gen wide" href="https://runwayml.com" target="_blank">
      <div class="card-head"><span class="card-name">Runway ML</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Generá clips de video desde texto o imagen. Ese clip es el material base que el sistema va a alterar en tiempo real cuando las piezas de origami se encuentren.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Tengo un video de 10 segundos. Dame código en p5.js para reproducirlo en loop y controlar su velocidad con una variable numérica."</p></div>
      <span class="card-tag">video generativo</span>
    </a>
    <a class="card gen" href="https://stability.ai/stable-diffusion" target="_blank">
      <div class="card-head"><span class="card-name">Stable Diffusion</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Generá imágenes fijas para fondos o texturas de la proyección. Podés hacer series que el sistema navega según el movimiento detectado.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame código p5.js para hacer crossfade entre dos imágenes controlado por una variable entre 0 y 1."</p></div>
      <span class="card-tag">imagen</span>
    </a>
    <a class="card gen" href="https://suno.com" target="_blank">
      <div class="card-head"><span class="card-name">Suno</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Generá música desde texto. El resultado puede ser la capa sonora del sistema, luego alterada en velocidad, pitch o volumen por el encuentro de las piezas.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame código JS con Web Audio API para reproducir un archivo y cambiar su velocidad en tiempo real."</p></div>
      <span class="card-tag">audio generativo</span>
    </a>
    <a class="card gen" href="https://app.udio.com" target="_blank">
      <div class="card-head"><span class="card-name">Udio</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Generación musical desde descripciones textuales. Alternativa a Suno con más control sobre estilo e instrumentación.</p>
      <span class="card-tag">música</span>
    </a>
    <a class="card gen" href="https://pika.art" target="_blank">
      <div class="card-head"><span class="card-name">Pika</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Generación de video desde imagen o texto. Buena para material base con movimientos suaves y atmosféricos. Más accesible que Runway.</p>
      <span class="card-tag">video</span>
    </a>
    <a class="card gen" href="https://freesound.org" target="_blank">
      <div class="card-head"><span class="card-name">Freesound</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Banco colaborativo de sonidos en Creative Commons. Texturas, ambientes, grabaciones de campo. Material directo para la capa sonora sin restricciones de uso.</p>
      <span class="card-tag">banco de audio</span>
    </a>
  </div>
</div>

<!-- 2: CAPTURAR + DETECTAR -->
<div class="slide" id="slide-2">
  <div class="sh">
    <span class="sh-num">02 — 03</span>
    <h2 class="sh-title">Capturar &amp; Detectar — la cámara ve el origami</h2>
    <span class="sh-desc">La cámara es el puente entre la mesa y el sistema.<br>Estas herramientas leen posición, movimiento y proximidad.</span>
  </div>
  <div class="grid">
    <a class="card cap wide" href="https://mediapipe-studio.webapps.google.com" target="_blank">
      <div class="card-head"><span class="card-name">MediaPipe</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Detecta objetos, manos y cuerpos desde la cámara del navegador en tiempo real. Devuelve coordenadas (x, y) de cada cosa detectada. Con esas coordenadas calculás la distancia entre las piezas de origami.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame código JavaScript con MediaPipe que abra la cámara, detecte dos objetos y calcule la distancia entre ellos en píxeles. Cuando baje de 100px, que cambie una variable llamada 'encuentro' a true."</p></div>
      <span class="card-tag">detección en tiempo real</span>
    </a>
    <a class="card cap" href="https://ml5js.org" target="_blank">
      <div class="card-head"><span class="card-name">ml5.js</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">ML para el navegador sin servidor. Clasificación de imágenes, detección de pose, segmentación. Funciona directo en el browser con p5.js. Muy documentado para artistas.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Con ml5.js y p5.js, abrí la cámara y detectá si hay un objeto en la mitad derecha o izquierda del frame."</p></div>
      <span class="card-tag">ml / browser</span>
    </a>
    <a class="card cap" href="https://p5js.org/reference/#/p5/createCapture" target="_blank">
      <div class="card-head"><span class="card-name">p5.js — createCapture</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">La forma más directa de abrir la cámara en p5.js. En minutos tenés el feed en el canvas y podés detectar movimiento por diferencia de frames consecutivos.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame código p5.js que abra la cámara, compare frames consecutivos y devuelva un número entre 0 y 1 que indique cuánto movimiento hay."</p></div>
      <span class="card-tag">entrada / cámara</span>
    </a>
    <a class="card cap" href="https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html" target="_blank">
      <div class="card-head"><span class="card-name">OpenCV.js</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Si los origamis tienen colores específicos, OpenCV puede rastrear cada pieza por separado y devolver su posición exacta. También detecta contornos y flujo óptico.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Con OpenCV.js, encontrá objetos de color rojo en el frame de la cámara y devolvé la posición del centro de cada uno."</p></div>
      <span class="card-tag">visión computacional</span>
    </a>
    <a class="card cap" href="https://github.com/tensorflow/tfjs-models/tree/master/hand-pose-detection" target="_blank">
      <div class="card-head"><span class="card-name">TF.js — Hand Pose</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Detecta 21 puntos de la mano en tiempo real. Útil si el sistema también reacciona a quien mueve las piezas, no solo a los objetos.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Con TensorFlow.js hand pose, abrí la cámara y dibujá un círculo en la punta del dedo índice mostrando su posición (x, y)."</p></div>
      <span class="card-tag">manos / gestos</span>
    </a>
  </div>
</div>

<!-- 3: CONECTAR -->
<div class="slide" id="slide-3">
  <div class="sh">
    <span class="sh-num">04</span>
    <h2 class="sh-title">Conectar — el encuentro altera el tiempo</h2>
    <span class="sh-desc">Tomás el valor de proximidad entre las piezas<br>y lo traducís en un cambio del audiovisual. Qué cambia, lo decidís vos.</span>
  </div>
  <div class="grid">
    <a class="card cod wide" href="https://p5js.org" target="_blank">
      <div class="card-head"><span class="card-name">p5.js — sistema completo en un archivo</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Con p5.js podés tener cámara, detección y modificación del audiovisual en un mismo archivo HTML. Es el camino más directo para un prototipo funcional dentro del día.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame un sketch en p5.js que: (1) abra la cámara, (2) calcule cuánto movimiento hay en el frame, (3) use ese valor para controlar la velocidad de un video y el volumen de un audio. Todo en un solo archivo HTML."</p></div>
      <span class="card-tag">prototipo completo</span>
    </a>
    <a class="card cod" href="https://derivative.ca/UserGuide/TouchDesigner" target="_blank">
      <div class="card-head"><span class="card-name">TouchDesigner</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Programación por nodos: conectás bloques sin escribir código. La cámara entra por un nodo, el movimiento sale como valor, ese valor controla efectos de video.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Explicame paso a paso cómo conectar un nodo de cámara con un nodo de velocidad de video en TouchDesigner. Soy principiante."</p></div>
      <span class="card-tag">nodal / sin código</span>
    </a>
    <a class="card cod" href="https://cycling74.com/products/max" target="_blank">
      <div class="card-head"><span class="card-name">Max / Jitter</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Programación visual para audio y video en vivo. Jitter procesa video frame a frame. Muy potente para manipulación sonora reactiva en tiempo real.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"En Max/MSP, cómo uso un valor numérico para cambiar el tempo de un clip de audio en tiempo real."</p></div>
      <span class="card-tag">audio / video live</span>
    </a>
    <a class="card cod" href="https://processing.org" target="_blank">
      <div class="card-head"><span class="card-name">Processing</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Entorno clásico de arte computacional. Miles de ejemplos de instalaciones físico-digitales. Buena opción si el equipo prefiere un entorno de escritorio.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame código Processing que abra la cámara, detecte movimiento por diferencia de frames y use ese valor para modificar la velocidad de un video."</p></div>
      <span class="card-tag">instalaciones</span>
    </a>
    <a class="card cod" href="https://threejs.org" target="_blank">
      <div class="card-head"><span class="card-name">Three.js — shaders reactivos</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Si la proyección va a tener profundidad o distorsión visual, Three.js permite shaders que reaccionan a variables en tiempo real.</p>
      <div class="card-prompt"><p class="card-prompt-label">pedile a Claude o ChatGPT</p><p class="card-prompt-text">"Dame un fragment shader en GLSL para Three.js que distorsione una imagen según un valor u_encuentro entre 0 y 1."</p></div>
      <span class="card-tag">3d / shaders</span>
    </a>
  </div>
</div>

<!-- 4: LENGUAJES -->
<div class="slide" id="slide-4">
  <div class="sh">
    <span class="sh-num">05</span>
    <h2 class="sh-title">Lenguajes — con IA para escribir el código</h2>
    <span class="sh-desc">No hace falta saber programar de antemano.<br>Conocer el lenguaje le da contexto a Claude o ChatGPT.</span>
  </div>
  <div class="grid cols3">
    <div class="lang-card">
      <span class="lang-name">JavaScript</span>
      <p class="lang-use">Corre en el navegador sin instalar nada. Base de p5.js, Three.js, ml5 y MediaPipe. El punto de partida más accesible del día.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://developer.mozilla.org/es/docs/Web/JavaScript/Guide" target="_blank">MDN guía</a>
        <a class="lang-link" href="https://javascript.info" target="_blank">javascript.info</a>
        <a class="lang-link" href="https://p5js.org/reference/" target="_blank">p5 referencia</a>
        <a class="lang-link" href="https://stackoverflow.com/questions/tagged/javascript" target="_blank">Stack Overflow</a>
      </div>
    </div>
    <div class="lang-card">
      <span class="lang-name">Python</span>
      <p class="lang-use">Muy usado en ciencia de datos y visión computacional. OpenCV, MediaPipe y TensorFlow tienen soporte nativo. Ideal si el equipo viene del mundo científico.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://docs.python.org/es/3/tutorial/" target="_blank">Tutorial oficial</a>
        <a class="lang-link" href="https://opencv-python-tutroals.readthedocs.io" target="_blank">OpenCV Python</a>
        <a class="lang-link" href="https://www.kaggle.com/learn" target="_blank">Kaggle Learn</a>
        <a class="lang-link" href="https://stackoverflow.com/questions/tagged/python" target="_blank">Stack Overflow</a>
      </div>
    </div>
    <div class="lang-card">
      <span class="lang-name">Processing (Java)</span>
      <p class="lang-use">Diseñado para artistas y diseñadores. Sintaxis simple, entorno propio, miles de ejemplos de instalaciones. El lenguaje histórico del arte computacional.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://processing.org/reference/" target="_blank">Referencia</a>
        <a class="lang-link" href="https://processing.org/examples/" target="_blank">Ejemplos</a>
        <a class="lang-link" href="https://discourse.processing.org" target="_blank">Comunidad</a>
        <a class="lang-link" href="https://openprocessing.org" target="_blank">OpenProcessing</a>
      </div>
    </div>
    <div class="lang-card">
      <span class="lang-name">GLSL</span>
      <p class="lang-use">El lenguaje de los shaders: corre en la GPU y genera efectos en tiempo real. Va dentro de p5.js o Three.js. Potente para distorsionar imagen reactivamente.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://book.of-shaders.com" target="_blank">Book of Shaders</a>
        <a class="lang-link" href="https://shadertoy.com" target="_blank">Shadertoy</a>
        <a class="lang-link" href="https://thebookofshaders.com/glossary/" target="_blank">Glosario GLSL</a>
      </div>
    </div>
    <div class="lang-card">
      <span class="lang-name">Max / Pure Data</span>
      <p class="lang-use">Programación por nodos y cables, sin texto. Para síntesis de audio y video en vivo. Pure Data es la versión gratuita y abierta de Max.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://cycling74.com/learn" target="_blank">Max Learn</a>
        <a class="lang-link" href="https://puredata.info/docs/tutorials" target="_blank">PD tutoriales</a>
        <a class="lang-link" href="https://forum.pdpatchrepo.info" target="_blank">PD comunidad</a>
      </div>
    </div>
    <div class="lang-card">
      <span class="lang-name">HTML + CSS</span>
      <p class="lang-use">La base de cualquier página. Si el sistema corre en el navegador, entender HTML básico permite armarlo todo en un archivo sin instalar nada.</p>
      <div class="lang-links">
        <a class="lang-link" href="https://developer.mozilla.org/es/docs/Learn" target="_blank">MDN Learn</a>
        <a class="lang-link" href="https://css-tricks.com" target="_blank">CSS-Tricks</a>
        <a class="lang-link" href="https://codepen.io" target="_blank">CodePen</a>
      </div>
    </div>
  </div>
</div>

<!-- 5: DATASETS -->
<div class="slide" id="slide-5">
  <div class="sh">
    <span class="sh-num">06</span>
    <h2 class="sh-title">Datasets — datos como material</h2>
    <span class="sh-desc">Datos científicos como capa de contenido.<br>Estructuras y series temporales para incorporar al audiovisual.</span>
  </div>
  <div class="grid">
    <a class="card dat" href="https://zenodo.org" target="_blank">
      <div class="card-head"><span class="card-name">Zenodo</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Repositorio científico del CERN. Datos de física, biología, ciencias sociales. Cada dataset tiene DOI. Búsqueda por disciplina o palabra clave.</p>
      <span class="card-tag">multidisciplinar</span>
    </a>
    <a class="card dat" href="https://openneuro.org" target="_blank">
      <div class="card-head"><span class="card-name">OpenNeuro</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Datos de neuroimagen (fMRI, EEG). Series temporales de actividad cerebral: ritmos, oscilaciones, patrones de percepción del tiempo.</p>
      <span class="card-tag">neurociencia</span>
    </a>
    <a class="card dat" href="https://opendata.cern.ch" target="_blank">
      <div class="card-head"><span class="card-name">CERN Open Data</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Trayectorias de partículas del LHC. Geometría visual muy rica para traducir en movimiento o estructura de la proyección.</p>
      <span class="card-tag">física de partículas</span>
    </a>
    <a class="card dat" href="https://data.nasa.gov" target="_blank">
      <div class="card-head"><span class="card-name">NASA Open Data</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Imágenes satelitales, datos de misiones, clima espacial, exoplanetas. APIs libres. Series temporales de fenómenos astronómicos.</p>
      <span class="card-tag">espacio</span>
    </a>
    <a class="card dat" href="https://www.gbif.org" target="_blank">
      <div class="card-head"><span class="card-name">GBIF — Biodiversidad</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Registros georreferenciados de especies a lo largo del tiempo. Distribución, migración, aparición y desaparición con dimensión temporal explícita.</p>
      <span class="card-tag">biodiversidad</span>
    </a>
    <a class="card dat" href="https://www.kaggle.com/datasets" target="_blank">
      <div class="card-head"><span class="card-name">Kaggle Datasets</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Miles de datasets listos para usar. Clima, movimiento, sonido, series temporales. El más accesible para prototipado rápido dentro del día.</p>
      <span class="card-tag">general</span>
    </a>
    <a class="card dat" href="https://archive.org" target="_blank">
      <div class="card-head"><span class="card-name">Internet Archive</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Millones de archivos de audio, video, imágenes y texto en dominio público. Material de archivo con capas históricas para incorporar a la proyección.</p>
      <span class="card-tag">archivo / cultura</span>
    </a>
    <a class="card dat" href="https://freesound.org" target="_blank">
      <div class="card-head"><span class="card-name">Freesound</span><span class="card-arrow">↗</span></div>
      <p class="card-desc">Sonidos en Creative Commons. Texturas sonoras, ambientes, grabaciones de campo. Material directo para la capa sonora.</p>
      <span class="card-tag">audio</span>
    </a>
  </div>
</div>

<!-- 6: GLOSARIO -->
<div class="slide" id="slide-6">
  <div class="sh">
    <span class="sh-num">07</span>
    <h2 class="sh-title">Glosario — términos del día</h2>
    <span class="sh-desc">Tocá cualquier término para ver su definición.<br>Sugerí uno nuevo y la IA lo genera al instante.</span>
  </div>
  <div class="glosario-wrap">
    <div class="glosario-left">
      <div class="glosario-list" id="glosario-list"></div>
      <div class="glosario-add">
        <p class="glosario-add-label">sugerí un término nuevo</p>
        <div class="glosario-add-row">
          <input id="gl-input" type="text" placeholder="ej: interpolación, latencia...">
          <button id="gl-btn">generar →</button>
        </div>
        <p class="glosario-status" id="gl-status"></p>
      </div>
    </div>
    <div class="glosario-panel" id="glosario-panel">
      <p class="glosario-panel-hint" id="gl-hint">← seleccioná un término</p>
      <span class="glosario-panel-name" id="gl-name"></span>
      <p class="glosario-panel-def" id="gl-def"></p>
      <p class="glosario-panel-ej" id="gl-ej"></p>
    </div>
  </div>
</div>

<!-- 7: TIPS -->
<div class="slide" id="slide-7">
  <div class="sh">
    <span class="sh-num">08</span>
    <h2 class="sh-title">Cómo hablarle a la IA — consejos para el día</h2>
    <span class="sh-desc">Prompts concretos para avanzar rápido<br>y no gastar tiempo ni tokens de más.</span>
  </div>
  <div class="grid">
    <div class="card tip"><div class="card-head"><span class="card-name">Referenciá, no repitas</span></div><p class="card-desc">No pegues el código completo cada vez. Señalá qué parte querés cambiar del código que ya escribió en el chat.</p><div class="card-prompt"><p class="card-prompt-label">en vez de pegar todo, decile</p><p class="card-prompt-text">"En el código que escribiste, modificá solo la función que detecta movimiento para que devuelva un valor entre 0 y 1."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pedile que te documente el código</span></div><p class="card-desc">Antes de usar el código que te generó, pedile que te explique cada parte. Así sabés dónde tocar si algo no funciona.</p><div class="card-prompt"><p class="card-prompt-label">prompt directo</p><p class="card-prompt-text">"Documentá este código. Para cada función, explicá en una línea qué hace y qué pasa si cambio sus parámetros."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pedile un mapa de parámetros</span></div><p class="card-desc">Cuando el código funciona y querés explorar efectos, pedile una lista de qué tocar y qué cambia. Las perillas del sistema.</p><div class="card-prompt"><p class="card-prompt-label">prompt directo</p><p class="card-prompt-text">"¿Qué variables puedo modificar para cambiar velocidad, color o intensidad del efecto? Dame el nombre, qué controla y qué rango tiene sentido."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pedile sliders para explorar en vivo</span></div><p class="card-desc">En lugar de editar el código cada vez que querés probar un valor, que agregue controles directamente en la pantalla.</p><div class="card-prompt"><p class="card-prompt-label">prompt directo</p><p class="card-prompt-text">"Agregá sliders HTML al lado del canvas para controlar los parámetros principales en tiempo real, mostrando el valor actual."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Construí en capas, no de una</span></div><p class="card-desc">Pedir todo junto genera código difícil de corregir. Pedí una parte, probala, y después seguís. Ahorra tiempo y tokens.</p><div class="card-prompt"><p class="card-prompt-label">cómo empezar</p><p class="card-prompt-text">"Primero hacé solo la parte que abre la cámara y muestra el feed. Cuando eso funcione, te pido la detección de movimiento."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pegá el error exacto de la consola</span></div><p class="card-desc">No describas el error con tus palabras. Copiá el mensaje exacto de la consola del navegador (F12 → Console).</p><div class="card-prompt"><p class="card-prompt-label">prompt directo</p><p class="card-prompt-text">"Este código me da el siguiente error en la consola: [pegá el error]. ¿Qué está mal y cómo lo corrijo?"</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pedile alternativas antes de comprometerte</span></div><p class="card-desc">Si no sabés qué camino tomar, pedile opciones con distinto nivel de complejidad. Elegís según el tiempo que tienen.</p><div class="card-prompt"><p class="card-prompt-label">prompt directo</p><p class="card-prompt-text">"Dame 3 formas de traducir la proximidad entre dos objetos en un cambio visual. Una muy simple, una intermedia y una elaborada."</p></div></div>
    <div class="card tip"><div class="card-head"><span class="card-name">Pedile que explique antes de escribir</span></div><p class="card-desc">Si te entrega código que no entendés, pedile primero que te diga qué va a hacer en lenguaje simple.</p><div class="card-prompt"><p class="card-prompt-label">antes de ejecutar</p><p class="card-prompt-text">"Antes de escribir el código, explicame en 3 pasos qué va a hacer y qué librerías va a usar. Después lo escribís."</p></div></div>
  </div>
</div>

</div><!-- /slides -->

<div id="nav">
  <button class="nav-btn" id="btn-prev">←</button>
  <div class="nav-sep"></div>
  <button class="nav-dot active" data-i="0"></button>
  <button class="nav-dot" data-i="1"></button>
  <button class="nav-dot" data-i="2"></button>
  <button class="nav-dot" data-i="3"></button>
  <button class="nav-dot" data-i="4"></button>
  <button class="nav-dot" data-i="5"></button>
  <button class="nav-dot" data-i="6"></button>
  <button class="nav-dot" data-i="7"></button>
  <div class="nav-sep"></div>
  <button class="nav-btn" id="btn-next">→</button>
  <div class="nav-sep"></div>
  <span id="slide-counter">0 / 7</span>
</div>

<script>
(function(){

/* ── NAV ── */
const slides  = document.querySelectorAll('.slide');
const dots    = document.querySelectorAll('.nav-dot');
const counter = document.getElementById('slide-counter');
let cur = 0;

function goTo(n){
  if(n < 0 || n >= slides.length) return;
  slides[cur].classList.remove('active');
  slides[cur].classList.add('exit');
  const prev = cur;
  setTimeout(()=> slides[prev].classList.remove('exit'), 600);
  cur = n;
  slides[cur].classList.add('active');
  dots.forEach((d,i) => d.classList.toggle('active', i===cur));
  counter.textContent = cur + ' / ' + (slides.length - 1);
}

document.getElementById('btn-prev').addEventListener('click', ()=> goTo(cur-1));
document.getElementById('btn-next').addEventListener('click', ()=> goTo(cur+1));
dots.forEach(d => d.addEventListener('click', ()=> goTo(+d.dataset.i)));
document.addEventListener('keydown', e => {
  if(e.key === 'ArrowRight' || e.key === ' ') goTo(cur+1);
  if(e.key === 'ArrowLeft') goTo(cur-1);
});
let tx = 0;
document.addEventListener('touchstart', e => { tx = e.touches[0].clientX; });
document.addEventListener('touchend',   e => { const dx = e.changedTouches[0].clientX - tx; if(Math.abs(dx) > 60) goTo(dx < 0 ? cur+1 : cur-1); });

/* ── EXTERNAL LINKS ── */
document.querySelectorAll('a[href]').forEach(a => {
  a.addEventListener('click', e => { e.preventDefault(); e.stopPropagation(); window.open(a.href, '_blank', 'noopener'); });
});

/* ── GLOSARIO ── */
const TERMINOS = [
  { t:'Debuggear',         d:'Encontrar y corregir errores en el código. Cuando algo no funciona, revisás el código o leés los mensajes de error para entender qué salió mal.',                                                             e:'Ejemplo: el video no reproduce. Abrís la consola (F12), ves un error en rojo, lo copiás y se lo pasás a la IA.' },
  { t:'Consola',           d:'Zona oculta del navegador donde aparecen los mensajes de error y los resultados de tu código. Se abre con F12 → pestaña Console.',                                                                            e:'Ejemplo: si escribís console.log(distancia) en tu código, el valor de distancia aparece ahí cada frame.' },
  { t:'Variable',          d:'Un nombre que guarda un valor que puede cambiar. Como una caja con etiqueta: la caja dice "distancia" y adentro hay un número que se actualiza todo el tiempo.',                                               e:'Ejemplo: let encuentro = false — empieza en falso y cambia a verdadero cuando las piezas se acercan.' },
  { t:'Función',           d:'Un bloque de código con nombre que hace una tarea específica. La llamás cuando la necesitás y puede devolver un resultado.',                                                                                   e:'Ejemplo: function calcularDistancia(a, b) recibe dos puntos y devuelve cuántos píxeles los separan.' },
  { t:'Parámetro',         d:'Un valor que le pasás a una función o una variable que podés cambiar para modificar el comportamiento del sistema. Los parámetros son las perillas del código.',                                               e:'Ejemplo: en drawCircle(x, y, tamaño, color), los cuatro parámetros definen cómo se dibuja el círculo.' },
  { t:'Frame / Fotograma', d:'Una imagen fija. Un video es una secuencia de frames. Comparar frames consecutivos de la cámara es la forma más simple de detectar movimiento.',                                                              e:'Ejemplo: si en el frame 1 el origami está a la derecha y en el frame 2 está más a la izquierda, hay movimiento.' },
  { t:'FPS',               d:'Cuántos frames por segundo procesa el sistema. A 30fps la cámara se lee 30 veces por segundo. Más FPS es más fluido pero consume más procesamiento.',                                                        e:'Ejemplo: frameRate(24) en p5.js fija el sistema a 24 fotogramas por segundo.' },
  { t:'Canvas',            d:'El área rectangular donde se dibuja todo. En p5.js y el navegador, el canvas es la hoja en blanco donde tu código pinta imágenes, formas, video y efectos.',                                                 e:'Ejemplo: createCanvas(1920, 1080) crea un canvas del tamaño de una pantalla Full HD.' },
  { t:'Loop / Bucle',      d:'El código que se repite una y otra vez. En p5.js, la función draw() es un loop que se ejecuta muchas veces por segundo y actualiza lo que se ve en pantalla.',                                                e:'Ejemplo: draw() le dice al sistema: revisá la cámara, calculá distancias, dibujá todo… y volvé a empezar.' },
  { t:'API',               d:'Una forma estandarizada de que dos programas se comuniquen. Cuando usás MediaPipe o Runway desde tu código, estás usando su API.',                                                                            e:'Ejemplo: la Web Camera API del navegador permite que tu código acceda a la cámara con permiso del usuario.' },
  { t:'Librería',          d:'Código que alguien más escribió y empaquetó para que vos lo uses sin escribirlo desde cero. p5.js, ml5 y Three.js son librerías: te dan funciones listas.',                                                  e:'Ejemplo: sin p5.js necesitarías cientos de líneas para abrir la cámara. Con ella, alcanza createCapture(VIDEO).' },
  { t:'Shader / GLSL',     d:'Un programa que corre en la GPU y calcula el color de cada píxel en tiempo real. Genera efectos visuales complejos reactivos a variables.',                                                                  e:'Ejemplo: un shader puede distorsionar la imagen según u_encuentro: cuanto más cerca las piezas, más se deforma la proyección.' },
  { t:'Render',            d:'Convertir datos o código en una imagen visible. Renderizar es cuando el sistema toma todos los cálculos y los convierte en lo que se ve en pantalla.',                                                       e:'Ejemplo: cada vez que draw() termina de ejecutarse, p5.js renderiza el resultado en el canvas.' },
  { t:'Tiempo real',       d:'Que ocurre sin demora perceptible. Un sistema en tiempo real procesa la entrada (cámara) y produce la salida (proyección) tan rápido que parece instantáneo.',                                               e:'Ejemplo: MediaPipe detecta la posición del origami y actualiza la proyección en el mismo momento en que se mueve.' },
  { t:'Coordenadas (x,y)', d:'Los valores que indican la posición de un punto en la pantalla. X es la distancia desde la izquierda, Y desde arriba. Con ellas calculás si dos objetos están cerca.',                                      e:'Ejemplo: si pieza1 está en (300, 200) y pieza2 en (310, 205), están casi en el mismo lugar: distancia ≈ 11px.' },
  { t:'Token (IA)',         d:'La unidad mínima que procesan los modelos de lenguaje. Aproximadamente una palabra. Cada conversación tiene un límite: si pegás código muy largo, agotás el contexto.',                                    e:'Ejemplo: en vez de pegar el código completo, referencialo: "en el código que escribiste, cambiá solo la función X".' },
  { t:'Prompt',            d:'El mensaje que le escribís a la IA para pedirle algo. Un buen prompt es específico, da contexto y describe el resultado esperado.',                                                                          e:'Ejemplo: "Dame código p5.js para detectar movimiento y devolver un número entre 0 y 1" es mejor que "código para la cámara".' },
  { t:'Crossfade',         d:'Transición suave entre dos elementos: mientras uno baja de visibilidad o volumen, el otro sube. Muy usado para mezclar imágenes o audio de forma fluida.',                                                   e:'Ejemplo: cuando el origami se acerca, la imagen A hace crossfade hacia la imagen B con opacidades cruzadas.' },
  { t:'Pitch',             d:'La altura tonal de un sonido: qué tan grave o agudo suena. Modificarlo en tiempo real hace que el encuentro de las piezas cambie la cualidad sonora del sistema.',                                           e:'Ejemplo: playbackRate(0.5) en Web Audio toca el sonido a mitad de velocidad y una octava más grave.' },
  { t:'Nodo',              d:'En programación visual (TouchDesigner, Max), un bloque que hace una operación. Los nodos se conectan con cables: la salida de uno es la entrada del siguiente.',                                              e:'Ejemplo: [cámara] → [detector de movimiento] → [valor 0-1] → [velocidad de video]. Cada bloque es un nodo.' },
  { t:'Feed de cámara',    d:'El flujo de imágenes en vivo que viene de la cámara. No es un video guardado: es lo que la cámara está viendo ahora mismo, cuadro por cuadro.',                                                             e:'Ejemplo: createCapture(VIDEO) en p5.js abre el feed y lo pone disponible para que tu código lo lea frame a frame.' },
];

const list   = document.getElementById('glosario-list');
const hint   = document.getElementById('gl-hint');
const glName = document.getElementById('gl-name');
const glDef  = document.getElementById('gl-def');
const glEj   = document.getElementById('gl-ej');
let activeEl = null;

function showTerm(item){
  hint.style.display   = 'none';
  glName.style.display = 'block';
  glDef.style.display  = 'block';
  glEj.style.display   = 'block';
  glName.textContent = item.t;
  glDef.textContent  = item.d;
  glEj.textContent   = item.e;
}

function makeBtn(item, isNew){
  const b = document.createElement('button');
  b.className = 'glosario-term-btn' + (isNew ? ' nuevo' : '');
  b.innerHTML = '<span>' + item.t + '</span><span style="font-size:.52rem;opacity:.4;">' + (isNew ? 'nuevo ' : '') + '→</span>';
  b.addEventListener('click', () => {
    if(activeEl) activeEl.classList.remove('active');
    activeEl = b;
    b.classList.add('active');
    showTerm(item);
  });
  list.appendChild(b);
  return b;
}

TERMINOS.forEach(item => makeBtn(item, false));

/* ── GENERAR TÉRMINO ── */
const glInput = document.getElementById('gl-input');
const glBtn   = document.getElementById('gl-btn');
const glSt    = document.getElementById('gl-status');

async function generarTermino(){
  const termino = glInput.value.trim();
  if(!termino) return;
  glBtn.disabled = true;
  glBtn.textContent = '...';
  glSt.style.color = 'var(--faint)';
  glSt.textContent = 'generando definición...';

  try {
    const res  = await fetch('/api/generate-term', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ termino })
    });
    if(!res.ok) throw new Error('error ' + res.status);
    const item = await res.json();
    const b = makeBtn(item, true);
    glInput.value = '';
    glSt.style.color = 'var(--ab)';
    glSt.textContent = '"' + item.t + '" agregado.';
    if(activeEl) activeEl.classList.remove('active');
    activeEl = b; b.classList.add('active'); showTerm(item);
    b.scrollIntoView({ behavior:'smooth', block:'nearest' });
  } catch(err) {
    glSt.style.color = 'var(--ad)';
    glSt.textContent = 'No se pudo generar. Intentá de nuevo.';
  }
  glBtn.disabled = false;
  glBtn.textContent = 'generar →';
}

glBtn.addEventListener('click', generarTermino);
glInput.addEventListener('keydown', e => { if(e.key === 'Enter') generarTermino(); });

})();
</script>
</body>
</html>

<template>
  <div>
    <a href="https://micro.cosasdev.comovas.es/svelte/" target="_blank" class="btn-101">
      NUEVO SVELTE APP
      <svg>
        <defs>
          <filter id="glow">
            <fegaussianblur result="coloredBlur" stddeviation="5"></fegaussianblur>
            <femerge>
              <femergenode in="coloredBlur"></femergenode>
              <femergenode in="coloredBlur"></femergenode>
              <femergenode in="coloredBlur"></femergenode>
              <femergenode in="SourceGraphic"></femergenode>
            </femerge>
          </filter>
        </defs>
        <rect />
      </svg>
    </a>

    <p style="
        font-size: x-small;
        color: aqua;
        font-family: 'Courier New', Courier, monospace;
        text-align: center;
      ">
      Este botón es un microservicio VUE en una página REACT
    </p>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      saludo: "Hello",
    };
  },
};
</script>

<style scoped>




/* FUENTE: https: //ui-buttons.web.app/ */
.btn-101,
.btn-101 *,
.btn-101 :after,
.btn-101 :before,
.btn-101:after,
.btn-101:before {
  border: 0 solid;
  box-sizing: border-box;
}

.btn-101 {
  -webkit-tap-highlight-color: transparent;
  -webkit-appearance: button;
  background-color: #000;
  background-image: none;
  color: #fff;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  font-size: 100%;
  font-weight: 900;
  line-height: 1.5;
  margin: 0rem;
  -webkit-mask-image: -webkit-radial-gradient(#000, #fff);
  padding: 0;
  text-transform: uppercase;
  text-align: center;
}

.btn-101:disabled {
  cursor: default;
}

.btn-101:-moz-focusring {
  outline: auto;
}

.btn-101 svg {
  vertical-align: middle;
}

.btn-101 [hidden] {
  display: none;
}

.btn-101 {
  --thickness: 0.3rem;
  --roundness: 1.2rem;
  --color: #186ae2;
  --opacity: 0.6;
  -webkit-backdrop-filter: blur(100px);
  backdrop-filter: blur(100px);
  background: none;
  background: hsl(216deg 81% 49% / 0.3);
  border: none;
  border-radius: var(--roundness);
  color: var(--color);
  cursor: pointer;
  display: block;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  word-spacing: 0.4rem;
  font-size: 1rem;
  font-weight: 500;
  padding: 0.8rem 3rem;
  position: relative;
  padding: 0.5rem 1rem 10rem 1rem;
}

.btn-101:hover {
  background: hsl(216deg 81% 49% / 00.4);
  filter: brightness(1.2);
}

.btn-101:active {
  --opacity: 0;
  background: hsla(0, 0%, 100%, 0.1);
}

.btn-101 svg {
  border-radius: var(--roundness);
  display: block;
  filter: url(#glow);
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}

.btn-101 rect {
  fill: none;
  stroke: var(--color);
  stroke-width: var(--thickness);
  rx: var(--roundness);
  stroke-linejoin: round;
  stroke-dasharray: 185%;
  stroke-dashoffset: 80;
  -webkit-animation: snake 2s linear infinite;
  animation: snake 2s linear infinite;
  -webkit-animation-play-state: paused;
  animation-play-state: paused;
  height: 100%;
  opacity: 0;
  transition: opacity 0.2s;
  width: 100%;
}

.btn-101:hover rect {
  -webkit-animation-play-state: running;
  animation-play-state: running;
  opacity: var(--opacity);
}

@-webkit-keyframes snake {
  to {
    stroke-dashoffset: 370%;
  }
}

@keyframes snake {
  to {
    stroke-dashoffset: 370%;
  }
}
</style>
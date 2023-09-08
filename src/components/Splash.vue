<template>
  <div class="splash">
    <h2 text-data="Welcome. . ." class="splash-text">Welcome. . .</h2>
  </div>
</template>

<script setup></script>

<style scoped>
.splash {
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--theme-primary);
  height: 0vh;
  width: 100%;
  overflow: hidden;
  animation: splashUp 3s cubic-bezier(0.13, 0.67, 0.7, 0.19) forwards;
}

@keyframes splashUp {
  0% {
    height: 100vh;
  }
  75% {
    height: 100vh;
  }
    100%{
    height: 0vh;
    display: none;
  }
}

.splash-text {
  font-size: 100px;
  font-weight: bold;
  position: relative;
  letter-spacing: 6px;
  color: var(--theme-primary);
  -webkit-text-stroke: 0.3px #dddddd36;
}
.splash-text::before {
  content: attr(text-data);
  font-weight: bold;
  position: absolute;
  top: 0;
  left: 0;
  width: 101%;
  height: 100%;
  color: white;
  -webkit-text-stroke: 0.3px #dddddd36;
  letter-spacing: 6px;
  overflow: hidden;
  border-right: 1px solid white;
  animation: textEffect 1.5s linear;
}

@keyframes textEffect {
    0%{width: 0;}
    100%{width: 101%;}
}

</style>

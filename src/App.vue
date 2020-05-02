<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
.jump {
  animation: jump 1s linear infinite;
  position: absolute;
  left: 50%;
}

@keyframes jump {
  0%,
  100% {
    bottom: 0;
  }
  50% {
    bottom: 20px;
  }
}
</style>

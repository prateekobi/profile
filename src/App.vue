<template>
  <div id="app">
    <router-view />
    <Toasts :show-progress="true" :rtl="false" :max-messages="5" :time-out="3000" :closeable="true"></Toasts>
  </div>
</template>

<style lang="scss">
.chevron {
  font-size: 40px;
  margin-top: 15px;
}

.jump {
  -webkit-animation: mover 1s infinite alternate;
  animation: mover 1s infinite alternate;
}
.jump {
  -webkit-animation: mover 1s infinite alternate;
  animation: mover 1s infinite alternate;
}
@-webkit-keyframes mover {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-10px);
  }
}
@keyframes mover {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-20px);
  }
}
</style>

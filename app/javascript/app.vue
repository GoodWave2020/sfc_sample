<template>
  <div id="app">
    <button style='text-align: center;' @click='show = !show'>切り替え</button>
    <br><br>
    <transition name='fade' mode='out-in'>
      <h1 v-if='show' style='text-align: center;'>{{ message }}</h1>
    </transition>
  </div>
</template>4

<script>
export default {
  data: function () {
    return {
      message: "Hello Vue.js",
      show: true
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: opacity 1s;
}
.fade-enter-to {
  opacity: 1;
}
.fade-leave {
  opacity: 1;
}
.fade-leave-active {
  transition: opacity 1s;
}
.fade-leave-to {
  opacity: 0;
}
</style>

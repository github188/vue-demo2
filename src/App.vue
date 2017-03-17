<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    name: 'app'
  }
</script>

<style lang="scss">
  #app {
    overflow-x: hidden;
    overflow-y: auto;
  }

  #app,
  body,
  html {
    height: 100%;
    width: 100%;
    overflow: hidden;
  }
</style>

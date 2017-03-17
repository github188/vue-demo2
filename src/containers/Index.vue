<template>
  <div id="container">
    <NavBar></NavBar>
    <router-view></router-view>
  </div>
</template>
<script>
  import NavBar from '../components/NavBar'
  export default {
    name: 'Index',
    data () {
      return {
      }
    },
    components: {
      NavBar
    }
  }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
  #container {
    height: 100%;
    overflow: auto;
    .content-wrapper {
      border-left: 0;
      overflow-x: hidden;
    }
  }
</style>

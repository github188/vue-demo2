<template>
  <div id="container">
    <NavBar></NavBar>
    <h1>Home</h1>
  </div>
</template>
<script>
  import NavBar from '../components/NavBar'
  export default {
    name: 'Home',
    data () {
      return {
        msg: 'Hello Vue!'
      }
    },
    computed: {
    },
    mounted () {
    },
    methods: {
    },
    components: {
      NavBar
    }
  }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
</style>

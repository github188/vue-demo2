<template>
  <nav class="navbar navbar-inverse">
    <div class="container-fluid">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#main-navbar">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <router-link to="/" class="navbar-brand">Index</router-link>
      </div>
      <div class="collapse navbar-collapse" id="main-navbar">
        <ul class="nav navbar-nav">
          <li><router-link to="/home">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
        </ul>
      </div><!-- /.navbar-collapse -->
    </div><!-- /.container-fluid -->
  </nav>
</template>
<script>
  export default {
    name: 'NavBar',
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
    }
  }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
</style>

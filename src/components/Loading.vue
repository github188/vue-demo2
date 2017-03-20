<template>
  <div class="loading_jump" v-if="isLoading">
    <div class="loading_jump1"></div>
    <div class="loading_jump2"></div>
  </div>
</template>
<script>
  export default {
    name: 'Loading',
    data () {
      return {
        msg: 'Hello Vue!'
      }
    },
    computed: {
      isLoading () {
        return this.$store.state.isLoading
      }
    },
    mounted () {
    },
    methods: {},
    components: {}
  }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
  .loading_jump {
    width: 1rem;
    height: 1rem;
    position: fixed;
    top: 50%;
    left: 50%;
    margin-top: -.5rem;
    margin-left: -.5rem;
    z-index: 9999;
    .loading_jump1 {
      width: 1rem;
      height: 1rem;
      position: absolute;
      background-image: url(../assets/loading.png);
      background-size: 100% auto;
      background-position: 0 -1rem;
      -webkit-animation: loadanimate 3.6s steps(6) infinite, updown .8s infinite;
      animation: loadanimate 3.6s steps(6) infinite, updown .8s infinite;
    }

    .loading_jump2 {
      width: 1rem;
      height: .7rem;
      position: absolute;
      bottom: -0.3rem;
      background: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48ZWxsaXBzZSBjeD0iNDgiIGN5PSIxMi40NjMiIGZpbGw9IiNEM0U2RkYiIGZpbGwtcnVsZT0iZXZlbm9kZCIgcng9IjQ3Ljg5IiByeT0iMTIuMzY5IiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyIDM4KSIvPjwvc3ZnPg==') no-repeat;
      background-size: 100% auto;
      -webkit-animation: updownbigsmall .8s infinite;
      animation: updownbigsmall .8s infinite;
    }
  }

  @-webkit-keyframes loadanimate {
    0% {
      background-position: 0 0rem;
    }
    100% {
      background-position: 0 -6rem;
    }
  }

  @keyframes loadanimate {
    0% {
      background-position: 0 0rem;
    }
    100% {
      background-position: 0 -6rem;
    }
  }

  @-webkit-keyframes updown {
    0% {
      -webkit-transform: translateY(0rem);
    }
    50% {
      -webkit-transform: translateY(-1rem);
    }
    100% {
      -webkit-transform: translateY(0rem);
    }
  }

  @keyframes updown {
    0% {
      transform: translateY(0rem);
    }
    50% {
      transform: translateY(-1rem);
    }
    100% {
      transform: translateY(0rem);
    }
  }

  @-webkit-keyframes updownbigsmall {
    0% {
      -webkit-transform: translateY(0rem) scale(1);
    }
    50% {
      -webkit-transform: translateY(.2rem) scale(.4);
    }
    100% {
      -webkit-transform: translateY(0rem) scale(1);
    }
  }

  @keyframes updownbigsmall {
    0% {
      transform: translateY(0rem) scale(1);
    }
    50% {
      transform: translateY(.2rem) scale(.4);
    }
    100% {
      transform: translateY(0rem) scale(1);
    }
  }
</style>

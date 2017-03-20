<template>
  <div id="app">
    <Loading></Loading>
    <transition name="fade" mode="out-in" v-if="showMe">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
  import Loading from './components/Loading'
  export default {
    name: 'app',
    data () {
      return {
        showMe: false // 是否展示当前页面
      }
    },
    components: {
      Loading
    },
    computed: {},
    mounted () {
      this.loadingtime(1500)
    },
    beforeUpdate () {
      this.loadingtime(300)
    },
    methods: {
      loadingtime (time) {
        // 设置当前状态为加载中
        this.$store.dispatch('setLoading', true)
        // 模拟请求等待
        setTimeout(() => {
          // 页面显示
          this.showMe = true
          this.$store.dispatch('setLoading', false)
        }, time)
      }
    }
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

  .fade-enter-active, .fade-leave-active {
    transition: opacity .3s;
  }

  .fade-enter, .fade-leave-active {
    opacity: 0;
  }
</style>

<template>
  <div id="app">
    <logo></logo>
    <div id="nav">
      <router-link to="/" exact>Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <transition name="fade">
      <router-view/>
    </transition>

  </div>
</template>
<script type="text/javascript">
  import Logo from './components/Logo.vue'
  export default {
  name: 'app',
  components: {
    Logo
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
    }
  }
}
</script>
<style lang="scss">
  @import '@/scss/base.scss';
</style>

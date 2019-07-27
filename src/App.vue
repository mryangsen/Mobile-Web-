<template>
  <div id="app">
    <keep-alive>
       <router-view class="router-view"></router-view>
    </keep-alive>
   
    <foot-bar v-show="$route.meta.footShow"></foot-bar>
  </div>
</template>
<script>
import FootBar from '@components/FootBar.vue'
export default {
  components:{
    FootBar
  }
}
</script>
<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.router-view{
  margin-bottom: 100px;
}
</style>

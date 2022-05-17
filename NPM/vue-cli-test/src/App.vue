<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="親から子" @app="child"/>
</template>

<script>
import HelloVue from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld:HelloVue
  },

  methods:{
    child:function(e){
      console.log(e)
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

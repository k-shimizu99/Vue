<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="親から子" @app="child"/>
  
  <div :key="index" v-for="(item,index) in items">
    <CardVue :id="item.id" :title="item.title" :image="item.image" :description="item.description" />
  </div>




</template>

<script>
import HelloVue from './components/HelloWorld.vue'
import CardVue from './components/CardSample.vue'

export default {
  name: 'App',
  components: {
    HelloWorld:HelloVue,
    CardVue
  },

  methods:{
    child:function(e){
      console.log(e)
    }
  },

  data(){
    return{
      items:[
        {
          id: 1,
          title: 'タイトル1',
          image: 'img1.jpg',
          description: '詳細1'
        },
        {
          id: 2,
          title: 'タイトル2',
          image: 'img2.jpg',
          description: '詳細2'
        },
        {
          id: 3,
          title: 'タイトル3',
          image: 'img3.jpg',
          description: '詳細3'
        }
      ]
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

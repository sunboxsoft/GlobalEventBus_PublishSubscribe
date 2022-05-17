<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button @click="handlePublish">pubsub-js publish</button>
    <router-view/>
  </div>
</template>

<script>
import pubsub from 'pubsub-js'
export default {
  name: 'App',
  methods:{
    handlePublish(){
      pubsub.publish('hiFun',888)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

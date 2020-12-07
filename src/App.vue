<template>
  <div id="app">
    <p>{{title}}</p>
    <navbar></navbar>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
    </ul>
  </div>
</template>

<script>
import navbar from './components/navbar.vue'
export default {
  name: 'App',

  data(){
    return{
      title : "First vue app"
    }
  },

  components:{
    navbar
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

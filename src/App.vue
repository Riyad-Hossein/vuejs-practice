<template>
  <div id="app">
    <p>{{title}}</p>
    <navbar :friends="friends" @dlt="remove"></navbar>

    <hr>
    All Friends
    <ol>
        <li v-for="(friend,index) in friends" :key="index" ><span >{{friend.name}}</span></li>
    </ol>
  </div>
</template>

<script>
import navbar from './components/navbar.vue'
export default {
  name: 'App',

  data(){
    return{
      title : "First vue app",
      friends:[
        {name: "A" , status : true},
        {name: "B" , status : true},
        {name: "C" , status : false},
        {name: "D" , status : true},
        {name: "E" , status : false},
      ]
    }
  },

  components:{
    navbar
  },
  
  methods:{
    remove(payload){
      //console.log(payload)
      this.friends = this.friends.filter(friend =>{
        return friend.name !== payload.name
      })
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

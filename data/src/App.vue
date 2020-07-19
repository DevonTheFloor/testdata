<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="one" v-show ="onesee">ONE</div>
    <div class="two" v-show ="twosee">TWO</div>
    <ButEv @name-customiser="newmethod"/>
  </div>
</template>

<script>

import ButEv from './components/ButEv'

export default {
  name: 'App',
  components: {
    ButEv
  },
  data(){
    return{
      onesee:true,
      twosee:false
    }
  },
  methods:{
    coucou(){
      alert('Réinitialisation ! ! !!!')
    },
    newmethod(payload){
      if(this.onesee === true){
        this.onesee = payload.onesee,
        this.twosee = payload.twosee
      } else{
        this.onesee = true,
        this.twosee = false,
        this.coucou()
      }
      
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: beige;
}
.one, .two{
  border: 3px solid blue;
  padding: 2%;
  background-color: cadetblue;
  margin: 1%;
}
.two{
  background-color: rgb(228, 173, 110);
}
</style>

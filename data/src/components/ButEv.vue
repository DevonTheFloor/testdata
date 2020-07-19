<template>
  <button class="clik" @click="emitEvent"> CLICK!</button>
</template>

<script>
export default {
  name: 'ButEv',
  methods:{
    emitEvent(){
      this.$emit('name-customiser',{onesee: false,
      twosee:true
      })
    }
  },
  beforeMount(){
    console.log("J'ARRIVE")
  },
  mounted(){
    console.log("Je Suis Là")
  }
}
</script>

<style lang="scss">
  .clik{
      border: 2px solid red ;
      padding: 1%;
    }
</style>
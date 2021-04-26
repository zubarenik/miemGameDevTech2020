<template>
  <div>
    <Navbar :curr_item="curr_item"/>
    <div class="container-fluid">
      <Title @show="handleTrigger('/')"/>
      <Description/>
      <Experts @show="handleTrigger('Experts')"/>
      <Date @show="handleTrigger('Date')"/>
      <Sponsors @show="handleTrigger('Sponsors')"/>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      curr_item: '/'
    }
  },
  methods:{
    handleTrigger(titl){
      this.curr_item = titl;
    }
  }
}
</script>

<style>
.container-fluid {
  padding: 0;
  min-height: 30vh;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
</style>

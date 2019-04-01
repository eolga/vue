<template>
  <div id="app">
   <p>{{ time }}</p> 
  </div>
</template>

<script>
export default {
  name: 'app',  
  data () {
    var d = new Date();
    return {
      time: d.getHours() + ':' + d.getMinutes()
    }
  }
} 
</script>

<style>
#app {
  //color: #f00; 
  //font-size: 120%; 
  //font-weight: bold;
}
</style>

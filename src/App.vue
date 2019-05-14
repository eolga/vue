<template> 
 <div id="app">
   <p>{{ time }}</p>
   <input type="button" v-on:click="clock" value="Показать время"/>
</div>
</template>

<script>
export default {
  name: 'app',  
  data() {
    
    return {
      time: '',
      timerID: ''
      }
    
  },
  
 methods: {
   clock : function updateTime(){
     var cd = new Date(); 
     this.timerID = setInterval(function() {
       this.time = zeroPadding(cd.getHours(), 2) + ':' + zeroPadding(cd.getMinutes(), 2) 
            + ':' + zeroPadding(cd.getSeconds(), 2)}, 1000)

            function zeroPadding(num, digit) {
            var zero = '';
            for (var i = 0; i < digit; i++) {
                zero += '0';
            }
            return (zero + num).slice(-digit);
        }
      }
   }
}
</script>

<style>
/*#app {
  
}*/
</style>

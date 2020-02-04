<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
  <button v-on:click='formatAMPM()'>CLICK TO TIMESTAMP</button>
  <div>{{cunt}}</div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data() {
    return {
      // moreInfo:false,
      // perklvlbool:true,
      hollowPointRounds: false,
      // lvl20:''name
      cunt: this.formatAMPM(new Date())
    };
  },

       methods: {
       test(){
        let a = new Date();
        let b = new Date();
        a.toLocaleTimeString();
        b.toLocaleTimeString()

        console.log(a)
        console.log(b)
      this.cunt = a

    
       },
       formatAMPM() {
      let date = new Date();
      let hours = date.getHours();
      let minutes = date.getMinutes();
      let seconds = date.getSeconds();
      let ampm = hours >= 12 ? 'pm' : 'am';
      hours = hours % 12;
      hours = hours ? hours : 12; // the hour '0' should be '12'
      minutes = minutes < 10 ? '0'+minutes : minutes;
      let strTime = hours + ':' + minutes + ':' + seconds + ' '+ ampm;

       this.cunt = strTime;

      return strTime;

     

  
}


      }
     

}
</script>

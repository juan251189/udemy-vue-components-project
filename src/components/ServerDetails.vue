<template>
  <div id="server-details">
    <div class="col-md-6">
      <p v-if="!server">Server details are unavailable </p>
      <p v-else>{{server.name}} selected | status {{server.status}}</p>
      <hr>
      <button @click="resetStatus">Switch status</button>

    </div>
  </div>
</template>

<script>
import {eventBus} from '../main';
export default{
  data(){
    return{
      server:null
    }
  },

  created(){
    eventBus.$on('serverSelected',(server)=>{

      this.server= server;
      console.log(this.server);
    });
  },
  methods:{
    resetStatus(){
      this.server.status='Normal';
    }
  }



}
</script>

<style>
</style>

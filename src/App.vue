<template>
  <div id="app">
    <div class="container">
      <h1 class="title">Server Status</h1>
      <hr>
<div class="row">
  <appServer></appServer>
  <app-server-details></app-server-details>

</div>


    </div>

  </div>
</template>

<script>

import Server from './components/Servers.vue';
import ServerDetails from './components/ServerDetails.vue';

export default {
  name: 'App',
  components: {
    appServer:Server,
    'app-server-details':ServerDetails
  }
}
</script>

<style>
#app {
padding-top: 3%;

}
.title{

}
</style>

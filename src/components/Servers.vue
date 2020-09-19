<template>
  <div id="servers">

      <div class="col-xs-12 col-sm-6" >
        <ul class="list-group" >
          <app-server v-for="(server,i) in servers" :key="i"
        class="server-list"
        :server="server">


        </app-server>
        </ul>
      </div>

  </div>
</template>
<script>

import Server from './Server.vue';
export default{
  data(){
    return{
      servers:[{
        name:'Server 1',
        id:1,
        status:'Active'
  },
    {
    name:'Server 2',

    id:2,
      status:'Active'


  },
{
    name:'Server 3',
    id:3,
      status:'Active'


  },
{
    name:'Server 4',
    id:4,
      status:'Active'


  }]
    }
  },
  components: {
    appServer:Server
  },
  methods: {
    changeStatus(server) {
      server.status='disable';

    }

  }

}

</script>

<style >




.server-active{
  color: #61a415;
}

.server-unavailable{
  color:#e03a0d;
}

.list-group{
  width: 100%;
  list-style-type: none;
}
</style>

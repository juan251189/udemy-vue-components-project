<template>
  <div id="servers">

      <div class="col-xs-12 col-sm-6" >
        <ul class="list-group" >
        <li v-for="(server,i) in servers" :key="i" class="server-list" @click="changeStatus(server)">
          {{server.name}}     |  <span :class="[server.status  === 'Active' ? 'server-active' : 'server-unavailable' ]">{{server.status}}</span>
        </li>
        </ul>
      </div>

  </div>
</template>
<script>
import {eventBus} from '../main';
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

    id:1,
      status:'Active'


  },
{
    name:'Server 3',
    id:1,
      status:'Active'


  },
{
    name:'Server 4',
    id:1,
      status:'Active'


  }]
    }
  },
  methods: {
    changeStatus:function(data){
      console.log(data);
      eventBus.$emit('changeStatus',data);
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

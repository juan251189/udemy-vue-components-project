<template>

    <li class="list-group"
    style="cursor:pointer;" @click="serverSelected">
        {{server.id}} | {{server.name}}
    </li>

</template>
<script>

import {eventBus} from '../main';
export default {
  data(){
      return{

      }
  },
  props: ['server'],
  methods: {
    serverSelected(){
      eventBus.$emit('serverSelected',this.server);
    }
  }
}
</script>
<style lang="scss" scoped>
</style>

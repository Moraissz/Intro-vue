<template>
<div id="CreateList">
  <ul>
   <li v-for=" (item, index) in list"  :key="item.id">
     <innerList v-bind:item="item" @remove = "$emit('remove',index)"></innerList>
   </li>
  </ul>
</div>
</template>

<script>
import InnerList from './InnerList'
export default {
  components: {
    InnerList
  },
  data() {
    return {};
  },
  props : {
    list : Array
  }
}
</script>

<style>

</style>

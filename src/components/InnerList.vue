<template>
  <div id = "inner-list">
    <span>{{item.name}}</span>
    <button @click= "$emit('remove')"> X </button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props : {
    item : Object
  }
};
</script>


<style>
</style>

<template>
  <li>
    <span>{{item.name}}</span>
    <button @click= "$emit('remove')"> X </button>
  </li>
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

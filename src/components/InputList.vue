<template>
<div id= "InputList">
<input type="text" v-model="data" @keyup.enter="$emit('addTodo',data)">
</div>
</template>


<script>
export default {
  data () {
    return {
      data: '',
    };
  },
  methods : {
    clearInput() {
      data = '';
    }
  }
}
</script>

<style>

</style>

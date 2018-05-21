<template>
<div id= "InputList">
<input type="text" v-model="data" @keyup.enter="handleEnter">
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
    handleEnter() {
      this.$emit('addTodo',this.data);
      this.data = '';

    }
  }
}
</script>

<style>

</style>

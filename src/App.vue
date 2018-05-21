<template>
<div id = "app">
  <ToDoListTitle> </ToDoListTitle>
  <InputList @addTodo= "addTodo"></InputList>
  <create-list>
    <InnerList v-for=" (item, index) in list" :key="item.index" v-bind:item="item" @remove = "removeItem(index)"></InnerList>
  </create-list>
</div>
</template>

<script>
import InnerList from './components/InnerList';
import ToDoListTitle from './components/ToDoListTitle';
import InputList from './components/InputList';
import CreateList from './components/CreateList'

export default {
  components : {
    CreateList,
    InnerList,
    ToDoListTitle,
    InputList
  },
  data () {
    return {
      data : '',
      list : [{name : 'Arroz'}, {name : 'Feijão'}, {name: 'Bife'}]
    }
  },
  methods : {
    addTodo(name) {
      this.list.push({name: name});
      this.data = '';
    },
    removeItem(index) {
      console.log(index);
      this.list.splice(index,1);
    }
  }
}
</script>

<style>

</style>

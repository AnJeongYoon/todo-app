<template>
  <div>
    {{ todoItems }}
  </div>
</template>

<script>
export default {
  data(){
    return{
      todoItems: []
    }
  },
  methods: {
    fetchTodoItems: function (){
      //var arr = [];
      for(var i = 0; localStorage.length; i++){
        var value = localStorage.key(i);
        //arr.push(value);
        this.todoItems.push(value);
      }
      //return arr;
     }
  },
  created: function(){
    this.fetchTodoItems();

    // localStorage.getItem();
    // axios.get();
    // $.ajax()
  }

}
</script>

<style>

</style>
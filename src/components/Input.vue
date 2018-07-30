<template>
  <div class="form-group">
    <input type="text" class="form-control"  placeholder="" v-model="value"/>
    <button type="button" class="btn btn-default" @click="add"> 添加 </button>
  </div>
</template>

<script>
  import { mapActions } from "vuex";
  export default{
    data(){
      return {
        value:"",
        id:0
      }
    },
    methods:{
      ...mapActions([
        'addTodo'
      ]),
      add(){
        let todo = {
          value: this.value,
          id: ++this.id
        };

        this.value = "";
        this.addTodo(todo)
      }
    }
  }
</script>

<style>
</style>

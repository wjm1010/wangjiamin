<template>
  <div class="todolist">
    <ul class="list-group">
      <li class="list-group-item" v-for="(todo, index) in todos" :key='index'>
        <span>{{todo.value}}</span>
        <button class="btn btn-default" @click="delate(index)"> 删除 </button>
      </li>
    </ul>
  </div>
</template>

<script>
  import { mapState,mapActions } from "vuex";

  export default{
    data(){
      return {}
    },
    methods:{
      ...mapActions([
        'delTodo'
      ]),
      delate(index){
        this.delTodo(index)
      }
    },
    computed:{
      ...mapState(['todos']) // 映射state
    }
  }
</script>

<style>
</style>


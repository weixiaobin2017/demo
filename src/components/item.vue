<template>
  <li class="list-group-item" >
    <div class="handle">
      <a href="javascript:;" @click="remove(index)">删除</a>
    </div>
    <p class="user"><span >{{todo.name}}</span><span>说:</span></p>
    <p class="centence">{{todo.content}}!</p>
  </li>
</template>

<script>
 export default {
     props:['todo','index','removeTodo'],
   methods:{
         remove (index) {
             if(confirm(`确定要删除${this.todo.name}吗？`))
             this.removeTodo(index)
         }
   }
 }
</script>

<style>

</style>

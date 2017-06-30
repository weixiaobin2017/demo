<template>
  <div class="col-md-8">
    <h3 class="reply">评论回复：</h3>
    <h2 style='display: none'>暂无评论，点击左侧添加评论！！！</h2>
    <ul class="list-group">
    <item v-for="(todo, index) in todos" :todo="todo" :index="index" :key="index" :remove-todo="removeTodo"></item>
    </ul>
  </div>
</template>

<script>
  import item from './item.vue'
export default {
    props :['todos','removeTodo'],
  components:{
        item
  }
}
</script>

<style>

</style>

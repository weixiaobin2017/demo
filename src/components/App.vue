<template>
  <div id="app">
    <div>
      <header class="site-header jumbotron">
        <div class="container">
          <div class="row">
            <div class="col-xs-12">
              <h1>请发表对Vue的评论</h1>
            </div>
          </div>
        </div>
      </header>
      <div class="container">
      <add :add="add"></add>
      <list :todos="todos" :remove-todo="removeTodo"></list>
      </div>
    </div>
  </div>
</template>

<script>
  import add from './add.vue'
  import list from  './list.vue'
  export default {
      data () {
          return {
              todos : [
                {name: '雄县人',content:'xxx'},
                {name: '洪洞人',content:'xxx'},
                {name: '隰县人',content:'xxx'},
              ]
          }
      },
    methods : {
          add(todo){
              this.todos.unshift(todo)
          },
      removeTodo (index) {
              this.todos.splice(index,1)
      }
    },
    components: {
      add,
      list
    }
  }
</script>

<style>

</style>

<template>
  <div class="col-md-4">
    <form class="form-horizontal">
      <div class="form-group">
        <label>用户名</label>
        <input type="text" class="form-control" placeholder="用户名" v-model="msg">
      </div>
      <div class="form-group">
        <label>评论内容</label>
        <textarea class="form-control" rows="6" placeholder="评论内容" v-model="msg1"></textarea>
      </div>
      <div class="form-group">
        <div class="col-sm-offset-2 col-sm-10">
          <button type="button" class="btn btn-default pull-right" @click="addd">提交</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
      props :['add'],
      data () {
          return {
              msg : '',
              msg1 : ''
          }
      },
    methods : {
          addd () {
              if(!this.msg.trim()||!this.msg1.trim()){
                  return
              }
              let todo = {
                  name : this.msg,
                content : this.msg1
              }
              this.add(todo)
            this.msg=''
            this.msg1=''
          }
    }
  }
</script>

<style>

</style>

<template>
  <div class="login-form">
    <div class="g-form-btn quit">
      <p>确认退出吗？</p>
      <a class="button" @click="okClick">确定</a>
      <a class="button" @click="cancelClick">取消</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    isShow:{
      type:Boolean,
      default:false
    }
  },
  methods:{
    okClick(){
      this.$emit('ok-quit')
    },
    cancelClick(){
      this.$emit('cancel-quit')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .quit{
    padding-left:0;
    text-align:center;
  }
  .quit p{
    line-height: 24px;
    font-size:16px;
    margin-bottom: 10px;
  }
</style>

<template>
  <div>
    <h1 v-html="message"></h1>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message:""
    }
  },
  created(){
    this.message=`&copy; 2022 Will Tengyuan Li`
  }
}
</script>
<style scoped>
div{
  height: 100px;
  background-color: antiquewhite;
}
</style>

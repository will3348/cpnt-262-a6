<template>
    <h1 v-html="message"></h1>
</template>
<script>
export default {
  data() {
    return {
      message:""
    }
  },
  created(){
    this.message=`&copy; 2022`
  }
}
</script>

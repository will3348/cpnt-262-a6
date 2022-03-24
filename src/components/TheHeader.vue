<template>
  <div>
    <h1 v-bind:class="{redHeader:hasUsedVBind}">{{ message }}</h1>
    <slot></slot>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "Will's Game House",
      hasUsedVBind: true,
    };
  },
};
</script>
<style scoped>
.redHeader{
  color: rgb(99, 15, 196);
}
h1{
 background-color: antiquewhite;
}
div{
  height: 100px;
}
</style>


<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/image.jpg">
    <HelloWorld msg="Best Price today"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

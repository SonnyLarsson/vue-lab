<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Hello there!"/>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'
export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  },
});
</script>

<template>
  <div class="hello">
    <p>
      THIS IS A TEST
    </p>
  </div>
  <GetJson />
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import GetJson from '../components/GetJson.vue';

  export default defineComponent({
  components: { GetJson },
    name: 'HelloWorld',
    props: {
      msg: {
        type: String,
        required: false,
      },
    },
    setup(props) {
      console.log(`MSG: ${props.msg}`);
    },
  });
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
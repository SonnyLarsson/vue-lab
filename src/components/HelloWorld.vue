<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      General Kenobi!
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <GetJson />
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import GetJson from './GetJson.vue';

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

<!-- Add "scoped" attribute to limit CSS to this component only -->
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

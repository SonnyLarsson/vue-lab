
<template>
  <div class="card text-center m-3">
    <h5 class="card-header">Get info from test file</h5>
    <div class="card-body">Info retrieved from JSON: {{testprop}}</div>
  </div>
</template>

<script>
export default {
  name: "GetJson",
  data() {
    return {
      testprop: null
    };
  },
  async created() {
    // GET request using fetch with async/await
    const response = await fetch('http://localhost:8080/uploads/test.json');
    const data = await response.json();
    console.log(`Data: ${data.testprop}`)
    this.testprop = data.testprop;
  }
};
</script>
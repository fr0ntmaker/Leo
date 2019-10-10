<template>
  <p v-if="tableInfo">
    API: <span class="api-name">{{ tableInfo }}</span>
  </p>
  <p v-else>
    Loading...
  </p>
</template>

<script>
  import axios from "axios";

  export default {
    data() {
      return {
        tableInfo: null,
        // version: null
      }
    },
    mounted() {
      axios.get('/private/data').then(response => {
      // axios.get('/').then(response => {
        this.tableInfo=response
        // this.name = response.data.name;
        // this.version = response.data.version;
      });
    },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .api-name {
    font-weight: bold;
  }
</style>

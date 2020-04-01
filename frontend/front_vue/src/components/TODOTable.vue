<template>
  <div>
    <h2>liste des TODO</h2>
    <table>
        <tr>
          <th>description</th>
        </tr>
        <tr v-for="TODO in TODOs" v-bind:key="TODO.id">
          <td>{{ TODO.description }}</td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "TODOsTable",
  data() {
    return {};
  },
  props: {
    TODOs: Array
  },
  created() {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
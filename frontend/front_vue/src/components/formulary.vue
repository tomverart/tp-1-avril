<template>
  <div>
    <h2>saisir TODO </h2>
    <label for="formulaireInput">TODO </label>
    <input v-model="formTODO" type="text" id="formulaireInput"/>
      <button v-on:click="addTODO">ADD</button>

  </div>
</template>

<script>

export default {
  name: 'newTODOForm',
  data() {
    return {
      formTODO: null 
    };
  },
  props: {},
  created() {},
  methods: {
    addTODO() {
      this.$emit("addTODO", {
        description: this.formTODO
      });
      this.formTODO = null;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

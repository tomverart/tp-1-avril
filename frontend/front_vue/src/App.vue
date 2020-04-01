<template>
  <div id="app">
    <h1>TP JS </h1>
        <formularyTODO v-on:addTODO="formulary" />
        <TODOTable :TODOs="TODOs" />
  </div>
</template>

<script>
import formularyTODO from './components/formulary.vue'
import TODOTable from "./components/TODOTable.vue"
//import {getTODO} from "./services/TODO.js"

export default {
  name: 'App',
  components: {
    formularyTODO,
    TODOTable
  },
  data() {
    return {
      TODOs: []
    };
  },
  
  methods: {
    
    formulary({description}) {
      this.TODOs = [
        ...this.TODOs,
      {
        description
      }
      ];
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

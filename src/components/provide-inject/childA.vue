<template>
    <div class="comp-container">
      <h1>Child A Component</h1>
      <div>Name: {{name}}</div>
      <childB/>
    </div>
  </template>
  
  <script>
  import {ref} from 'vue'
  import childB from './childB.vue'

  export default {
    name: 'childA',
    components:{
        childB
    },
    setup() {
      const name = ref('Raghuvar')
      name.value = 'Anshul'
      return {
        name
      }
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  .header {
      color: green
    }
  </style>
  
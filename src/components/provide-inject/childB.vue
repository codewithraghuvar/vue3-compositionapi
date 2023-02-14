<template>
    <div class="comp-container">
      <h1>Child B Component</h1>
      <div>privide inject: {{name}}</div>
      
    </div>
  </template>
  
  <script>
  import { inject} from 'vue'
  export default {
    name: 'childB',
    inject: ['username'],
    setup(){
      const name = inject('username')
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
  
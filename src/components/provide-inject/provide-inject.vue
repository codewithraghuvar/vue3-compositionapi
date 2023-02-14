<template>
    <div class="comp-container">
      <h1>Provide Inject Component</h1>
      <div>name: {{name}}</div>
      <childA/>
    </div>
</template>
  
  <script>
  import { provide } from 'vue'
  import childA from './childA.vue'
  export default {
    name: 'provide-inject',
    components:{
        childA
    },
    setup(){
      provide('username', 'provide raghuvar') 
      
         
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  .header {
      color: green
    }
  </style>
  
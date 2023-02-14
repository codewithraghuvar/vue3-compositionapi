<template>
    <div class="comp-container">
      <h1>Ref Component</h1>
      <div>Name: <input type="text" ref="inputRef"/></div>
    </div>
  </template>
  
  <script>
  import {ref , onMounted} from 'vue'
  export default {
    name: 'refs-component',
    setup(){
      const inputRef = ref(null)
      onMounted(()=>{
        inputRef.value.focus()
      })
      return {
        inputRef
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
  
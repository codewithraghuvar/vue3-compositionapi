<template>
    <div class="comp-container">
      <h1>Reactive Component</h1>
      <div>First Name: {{state.firstName}}</div>
      <div>last Name: {{state.lastName}}</div>
      <div>hero Name: {{state.heroName}}</div>
    </div>
  </template>
  
  <script>
  import { reactive,toRefs } from 'vue'
  export default {
    name: 'reactive-component',
    setup(){
      const state = reactive({
        r_firstName: 'Raghuvar',
        r_lastName: 'Visht',
        r_heroName: 'heroname'
      })

    setTimeout(() => {
        state.r_firstName = 'Anshul'
        state.r_lastName = 'Singh'

    }, 2000);
    
    return toRefs(state)
     /* return {
        firstName: state.r_firstName,
        lastName: state.r_lastName
      }*/
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  .header {
      color: green
    }
  </style>
  
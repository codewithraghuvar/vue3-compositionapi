<template>
    <div class="comp-container">
      <h1>vmodel Component</h1>
      <div>First Name: {{firstName}}</div>
      <div>last Name: {{lastName}}</div>
      <div>hero Name: {{heroName}}</div>
    </div>
  </template>
  
  <script>
  import { reactive , toRefs} from 'vue'
  export default {
    name: 'vmodel-component',
    setup(){
        const state = reactive({
            firstName: 'Raghuvar',
            lastName: 'Visht',
            heroName: 'heroname'
        })

        setTimeout(() => {
            state.firstName = 'Anshul'
            state.lastName = 'Singh'

        }, 2000);
        
        return {
            ...toRefs(state)
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
  
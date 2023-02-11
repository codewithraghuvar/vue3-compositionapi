<template>
    <div class="comp-container">
      <h1>Method Component</h1>
      <div>Count: {{count}}</div>
      <button @click="incrementCount">Increment Count</button>
      <br/><br/><br/>
      <div>Firstname: {{firstName}}</div>
      <div>Lastname: {{lastName}}</div>
      <button @click="changeName">Change Name</button>

    </div>
</template>
  
  <script>
  import { ref, reactive, toRefs} from 'vue'
  export default {
    name: 'method-component',
    setup(){
      const count = ref(0)      
      function incrementCount(){
        count.value++
      }

      const state = reactive({
        firstName: 'Raghuvar',
        lastName: 'Visht'
      })

      function changeName() {
        state.firstName = 'Amit'
        state.lastName = 'Singh'
      }

      return {
        count,
        incrementCount,
        ...toRefs(state),
        changeName,
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
  
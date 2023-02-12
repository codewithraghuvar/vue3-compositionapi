<template>
    <div class="comp-container">
      <h1>vmodel Component</h1>
      <div>
       <div> Firstname : <input type="text" placeholder="First Name" v-model="firstName"/></div>
       <div>  Lastname: <input type="text" placeholder="Last Name" v-model="lastName"/></div>
       <div> Country: <input type="text" placeholder="Country" v-model="country"/></div>

      </div>
    </div>
  </template>
  
  <script>
  import { reactive, ref, toRefs} from 'vue'
  export default {
    name: 'vmodel-component',
    setup(){
        const country = ref('')
        const state = reactive({
            firstName: '',
            lastName: ''        
        })

        return {
          country,
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
  
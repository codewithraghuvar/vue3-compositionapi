<template>
    <div class="comp-container">
      <h1>Computed Component</h1>
      <div>
        Ref Computed
       <div> Firstname : <input type="text" placeholder="First Name" v-model="fname"/></div>
       <div> Lastname: <input type="text" placeholder="Last Name" v-model="lname"/></div><br/>
       <div> FullName: {{refFullName}}</div>
      </div>
      <div>
        Reactive computed
       <div> Firstname : <input type="text" placeholder="First Name" v-model="firstName"/></div>
       <div> Lastname: <input type="text" placeholder="Last Name" v-model="lastName"/></div><br/>
       <div> FullName: {{fullName}}</div>
      </div>
    </div>
  </template>
  
  <script>
  import {ref, reactive, computed, toRefs} from 'vue'
  export default {
    name: 'computed-component',
    setup(){
        const fname = ref('')
        const lname = ref('')

        const refFullName = computed(function(){
            return `${fname.value} ${lname.value}`
        })
        
        const state = reactive({
            firstName: '',
            lastName: ''        
        })
        const fullName = computed(function(){
            return `${state.firstName} ${state.lastName}`
        })
        return {
            fname,
            lname,
            refFullName,
            fullName,
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
  
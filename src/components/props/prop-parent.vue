<template>
    <div class="comp-container">
       FirstName:  <input type="text" v-model="firstName"/>
       LastName:  <input type="text" v-model="lastName"/>
      <propChild :fname="firstName" :lname="lastName"/>
    </div>
  </template>
  
  <script>
  import {ref} from 'vue'
  import propChild from './prop-child.vue'
  export default {
    name: 'prop-parent',
    components:{
        propChild
    },
    setup(){
        const firstName = ref('')
        const lastName = ref('')

        return {
            firstName,
            lastName
        }
    }
    
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>
  
<template>
    <div class="comp-container">
      <div>hello {{ fullName }}</div>
    </div>
  </template>
  
  <script>
  import {computed} from 'vue'
  export default {
    name: 'prop-child',
    props:['fname','lname'],
    setup(props){
        // this.fname will not work as setup method call very early before calling props
        const fullName = computed(()=>{
            return `${props.fname} ${props.lname}`
        })

        return {
            fullName
        }
    }
    
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>
  
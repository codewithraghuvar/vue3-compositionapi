<template>
    <div class="comp-container">
      <h1>watch Component</h1>
      <div>
        ref Watch Computed
        <div> Firstname : <input type="text" placeholder="First Name" v-model="fname"/></div><br/>
        <div> Lastname: <input type="text" placeholder="Last Name" v-model="lname"/></div>
        <div> Options: <input type="text" placeholder="Options Name" v-model="options.name"/></div>
      </div>
      <div>
        Reactive Watch Computed
        <div> Firstname : <input type="text" placeholder="First Name" v-model="firstname"/></div><br/>
        <div> Lastname: <input type="text" placeholder="Last Name" v-model="lastname"/></div>
        <div> City: <input type="text" placeholder="City" v-model="address.city"/> </div>
      </div>
    </div>
  </template>
  
  <script>
  import {ref, reactive, toRefs, watch } from 'vue'
  export default {
    name: 'watch-component',
    setup(){
        // ref way to se watch
        const fname = ref('')
        const lname = ref('')
        const options = ref({name:''})

        watch([fname, lname, options], (newvalue, oldvalue) => {
            console.log('fname newvalue==' + newvalue[0] + '== fname oldvalue==' + oldvalue[0])
            console.log('lname newvalue==' + newvalue[1] + '==lname oldvalue==' + oldvalue[1])
            console.log('options newvalue==' + newvalue[2]?.name  + '==options oldvalue==' + oldvalue[2]?.name)
        },
        {
            immediate: true,
            deep:true
        })

        const state = reactive({
            firstname: '',
            lastname: '',
            address: {
                city: ''
            }
            
        })

        watch(
        ()=> {            
            return {...state}
        }, (newvalue, oldvalue) => {
            console.log('firstname newvalue==' + newvalue.firstname + '== firstname oldvalue==' + oldvalue.firstname)
            console.log('lastname newvalue==' + newvalue.lastname + '==lastname oldvalue==' + oldvalue.lastname)
            console.log('city newvalue==' + newvalue.address.city + '==city oldvalue==' + oldvalue.address.city)
        },
        {
            deep: true
        })
        return {
            fname,
            lname,
            options,
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
  
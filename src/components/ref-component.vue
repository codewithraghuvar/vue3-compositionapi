<template>
  <div class="comp-container">
    <h1>Ref Component</h1>
    <div>Name: {{name}}</div>
  </div>
</template>

<script>
import {ref} from 'vue'
export default {
  name: 'ref-component',
  setup(){
    const name = ref('Raghuvar')
    name.value = 'Anshul'
    return {
      name
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

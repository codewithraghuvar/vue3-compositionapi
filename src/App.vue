<template>   
  <refComponent/>
  <reactiveComponent/>
  <methodComponent/>
  <vmodelComponent/>
</template>

<script>
import refComponent from './components/ref-component.vue'
import reactiveComponent from './components/reactive-component.vue'
import methodComponent from './components/method-component.vue';
import vmodelComponent from './components/vmodel-component.vue';

export default {
  name: 'App',
  components: {
    refComponent,
    reactiveComponent,
    methodComponent,
    vmodelComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.full-border {
 border: 1px solid #2c3e50;
 padding: 1rem;
 margin:1rem 0;
}

.comp-container {
  border: 1px solid #2c3e50;
  margin: 1rem;
  padding: 1rem;
}
</style>

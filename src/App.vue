<template>  
  <propParent/>
  <refsComponent/>
  <provideInject/>
  <WatchComponent/>
  <computedComponent/>
  <vmodelComponent/>
  <methodComponent/>
  <refComponent/>
  <reactiveComponent/>  
</template>

<script>
import refComponent from './components/ref-component.vue'
import reactiveComponent from './components/reactive-component.vue'
import methodComponent from './components/method-component.vue';
import vmodelComponent from './components/vmodel-component.vue';
import computedComponent from './components/computed-component.vue';
import WatchComponent from './components/watch-component.vue';
import provideInject from './components/provide-inject/provide-inject.vue';
import refsComponent from './components/refs-component.vue';
import propParent from './components/props/prop-parent.vue';

export default {
  name: 'App',
  components: {
    refComponent,
    reactiveComponent,
    methodComponent,
    vmodelComponent,
    computedComponent,
    WatchComponent,
    provideInject,
    refsComponent,
    propParent
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

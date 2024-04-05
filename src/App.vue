<template>
  <div id="app">
    <h1>Dynamic Components</h1>
    <button @click="activeTab = 'TabA'">TabA</button>
    <button @click="activeTab = 'TabB'">TabB</button>
    <button @click="activeTab = 'TabC'">TabC</button>

    <component  :is="activeTab"/>
    
  </div>
</template>

<script>
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';
export default {
  name: 'App',
  components:{
    TabA,
    TabB,
    TabC
  },
  data(){
    return{
      activeTab:'TabA'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <EnterPage msg="Enter"/>
  <hr>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue';
  import EnterPage from './components/EnterPage.vue';

  export default {
    name: 'App',
    components: {
      HelloWorld, EnterPage,
    }
  }
</script>

<style lang="less">
  .btn-outline-info:hover {
    color: white;
  }
  
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>

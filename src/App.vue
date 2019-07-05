<template>
  <div id="app">
    <Language></Language>
  </div>
</template>

<script>
  import Language from "./components/Language";

  export default {
    name: 'App',
    components: {
      Language
    }
  }
</script>
<style>
  #app {
    display: flex;
    justify-content: center;
    margin-top: 100px;
    text-align: center;
    font-family: 'Open Sans', sans-serif;
  }
</style>

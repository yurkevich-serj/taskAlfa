<template>
  <form v-on:submit.prevent="$emit('inputChange', $event)">
    <input :value="languages" type="text" :placeholder="languages" id="language">
    <button type="submit">Submit</button>
  </form>
</template>

<script>
  export default {
    props: ['languages']
  }
</script>

<style>
  input {
    margin: 15px;
    border-radius: 10px;
    height: 25px;
    border: 3px solid black;
  }

  button {
    height: 25px;
    background-color: #FFE0ED;
    border-radius: 10px;
    color: blue;
    border: 3px solid #FF645F;
  }
</style>

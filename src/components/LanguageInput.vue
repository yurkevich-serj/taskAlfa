<template>
  <form v-on:submit.prevent="$emit('inputChange', $event)">
    <input type="text"  placeholder="Type language" id="language">
    <button type="submit">Submit</button>
  </form>
</template>

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

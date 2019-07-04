<template>
  <div>
    <div class="text">Your choise is {{currentLanguage}}</div>
    <nav class="list">
      <ul class="mama">
        <li>Touch me
          <ul>
            <li v-on:click="changeCurrentLanguage" v-for="language in languages">{{language}}</li>
          </ul>
        </li>
      </ul>
    </nav>
    <LanguageInput v-if="currentLanguage" @inputChange="changeCurrentLanguage"></LanguageInput>
  </div>
</template>

<script>
  import LanguageInput from './LanguageInput'
  export default {
    name: 'Language',
    components: {
      LanguageInput
    },
    methods: {
      changeCurrentLanguage: function(event) {
        if(event.type == 'submit') {
          if(this.languages.includes(event.target.language.value)) {
            this.currentLanguage = event.target.language.value;
          } else {
            alert('Çhoose language from the list');
          }
        } else {
          this.currentLanguage = event.target.innerText;
        }
      },
    },
    data: function (){
      return {currentLanguage: null, languages: ['English','Spanish','Italian']};
    }
  }
</script>

<style>
  .text {
    font-size: 46px;
    color: crimson;
  }
  .mama {
    border: 3px solid black;
  }
  .list ul {
    font-size: 35px;
    margin: 0;
    padding: 5px;
    list-style: none;

  }
  .list ul li {
    cursor: pointer;

  }
  .list ul ul{
    display: none;
    list-style: none;
  }
  .list li:hover ul{
    display:flex;
    flex-direction: column;
  }
</style>


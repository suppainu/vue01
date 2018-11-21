<template>
  <div>
    <button v-on:click='onClick()'>click</button>
    {{ clickResult }}

    <br>
      <input v-on:change='onChange($event)' placeholder='change'>
    {{ changeResult }}

    <br>
      <input @input='onInput($event)' placeholder='input'>
    {{ inputResult }}

    <br>

    <input @keyup='onKeyup($event)' placeholder="keyup">
    {{ keyupResult }}
  </div>
</template>

<script>
export default {
  data(){
    return{
      clickResult: '',
      changeResult: '',
      inputResult: '',
      keyupResult: ''
    }
  },
  methods: {
    onClick(){
      this.clickResult = 'clicked';
    },
    onChange(e){
      this.changeResult = e.target.value;;
    },
    onInput(e){
      this.inputResult = e.target.value;;
    },
    onKeyup(e){
      this.keyupResult = e.target.value;
    }
  }
}
</script>
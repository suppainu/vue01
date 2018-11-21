<template>
  <div>
    <h3>{{ title }}</h3>
  <ul>
    <li><a v-bind:href="url1">Vue</a></li>
    <li><a :href="url2">Vuetify</a></li>
  </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      title:'Vue sites',
      url1:'https://vuejs.org/',
      url2:'https://vuetifyjs.com/'
    }
  }
}
</script>
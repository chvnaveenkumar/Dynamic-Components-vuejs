<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">AUthor</button>
        <button @click="selectedComponent = 'appNew'">New Quote</button>
        <p>{{ selectedComponent }}</p>
        <component :is="selectedComponent"></component>
      </div>
    </div>
  </div>
</template>

<script>
import appQuote from './components/Quote.vue'
import appAuthor from './components/Author.vue'
import appNew from './components/New.vue'

export default {
  name: 'App',
  data: function(){
    return {
    selectedComponent: 'appQuote'
    }
  },
  components: {
    appQuote,
    appAuthor,
    appNew
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

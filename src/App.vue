<template>
  <div id="app">
    <!-- We deleted all of the default stuff in this div and added the following code -->
    <h1>Example of Webpack Simple</h1>
    <light v-on:lightClicked="catchLight" />
  </div>
</template>

<script>
// 'import' is new code
import light from './components/light.vue';

export default {
  name: 'app',
   // 'components' code is new, it lists out that this is a component that vue should use
  components: {
    light
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    catchLight: function(color) {
      alert('light was clicked...' + color)
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

<template>
<div id="app">
    <div>
      <form>
	<input type="text" v-model="number">
      </form>
      <p> {{ number }} </p>
    </div>
    <HelloWorld id="first" msg="Welcome to Your Vue.js App"/>
    <OtherComponent id="second" msg="This is your other component"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import OtherComponent from './components/OtherComponent.vue'

export default {
  data: function() {
    return {
      number: 0
    }
  },
  name: 'app',
  components: {
    HelloWorld,
    OtherComponent
  },
}
</script>

<style>
#app {
  display: grid;
  grid-column-gap: 500px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#first {
  display: grid;
  grid-column-start: 0;
  grid-column-end: 1;
}
#second {
  display: grid;
  grid-column-start: 1;
  grid-column-end: 2;
}
</style>

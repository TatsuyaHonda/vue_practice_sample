<template>
  <div id="app">
    <HelloWorld :title="message" />
    <hr>
    <button @click="doAction">change title</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
  },
  data: function () {
    return {
      message: "HELLO",
    };
  },
  methods: {
    doAction: function () {
      var inputValue = prompt("new title:");
      this.message = inputValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

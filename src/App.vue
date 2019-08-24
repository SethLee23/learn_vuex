<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png" @click="dosth">
    <span>{{count}}</span>
  </div>
</template>
<script>
import { store } from "./store/main.js";
export default {
  name: "App",
  computed: {
    count() {
      return store.state.count;
    }
  },
  // store: store,
  methods: {
    dosth() {
      store.dispatch("asyncIncrement");
      console.log(store.state.count); // -> 1
    }
  }
};
</script>$createElement

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

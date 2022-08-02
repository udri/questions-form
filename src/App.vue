<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <QuestionsList />
  </div>
</template>

<script>
import QuestionsList from "./components/QuestionsList.vue";

export default {
  name: "App",
  components: {
    QuestionsList,
  },
};
</script>

<style>
body {
  background: #2c3e50;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #9ebddc;
  margin-top: 60px;
}
</style>

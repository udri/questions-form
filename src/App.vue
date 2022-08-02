<template>
  <div id="app">
    <MiniHeader />
    <QuestionsList />
  </div>
</template>

<script>
import MiniHeader from "./components/MiniHeader.vue";
import QuestionsList from "./components/QuestionsList.vue";

export default {
  name: "App",
  components: {
    MiniHeader,
    QuestionsList,
  },
};
</script>

<style>
body {
  background: #2c3e50;
}
#app {
  font-family: "Source Sans Pro", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #9ebddc;
}
</style>

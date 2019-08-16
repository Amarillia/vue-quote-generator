<template>
  <div id="app">
    <Header headerTitle="Random Quote Generator" />
    <Main msg="Generate random new quotes and brighten up your day." />
  </div>
</template>

<script>
import Main from "./components/AppMain";
import Header from "./components/AppHeader";

export default {
  name: "app",
  components: {
    Main,
    Header
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto+Condensed");

html,
body {
  font-family: "Roboto Condensed", sans-serif;
  background-color: darkseagreen;
}

#app {
  font-family: "Roboto Condensed", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <assignment-buttons msg="Hi" />
  </div>
</template>

<script>
import AssignmentButtons from "@/components/AssignmentButtons.vue";

export default {
  name: "App",
  components: {
    AssignmentButtons,
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

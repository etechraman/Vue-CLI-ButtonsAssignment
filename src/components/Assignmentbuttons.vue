<template>
  <div id="example-1">
    <p>{{ message }}</p>
    <buttoncounter
      :text="'Primary'"
      @handle-click="reverseMessage()"
      :activeColor="this.activeColor1"
    />
    <buttoncounter
      :text="'Secondary'"
      @handle-click="greet()"
      :activeColor="this.activeColor2"
    />
  </div>
</template>

<script>
import buttoncounter from "./buttoncounter.vue";

export default {
  name: "Assignmentbuttons",
  components: {
    buttoncounter,
  },
  data: () => {
    return {
      message: "Hello Vue.!",
      activeColor1: "grey",
      activeColor2: "green",
    };
  },
  methods: {
    reverseMessage() {
      this.message = this.message
        .split("")
        .reverse()
        .join("");
    },
    greet() {
      alert(this.message + "!");
    },
  },
};
</script>

<style>
button {
  background-color: #0069d9;
  color: #ffffff;
  margin: 22px 16px;
  padding: 22px 40px;
}
</style>

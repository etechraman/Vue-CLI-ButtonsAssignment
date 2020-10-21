<template>
  <div>
    <p>{{ message }}</p>
    <base-button @handle-click="reverseMessage()" />
    <base-button
      :propText="'Secondary'"
      @handle-click="greet()"
      :propColor="activeColor"
    />
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "AssignmentButtons",
  components: {
    BaseButton,
  },
  data: () => {
    return {
      message: "Hello Vue.!",
      activeColor: "grey",
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

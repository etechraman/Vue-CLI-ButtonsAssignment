<template>
  <div>
    <button
      @click="$emit('handle-click')"
      :style="{ 'background-color': propColor }"
    >
      {{ propText }}
    </button>
  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    propText: {
      type: String,
      default: "Primary",
    },
    propColor: {
      type: String,
      default: "#0069d9",
    },
  },
};
</script>

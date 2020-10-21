<template>
  <div>
    <button
      @click="$emit('handle-click')"
      :style="{ 'background-color': activeColor }"
    >
      {{ text }}
    </button>
  </div>
</template>

<script>
export default {
  name: "Base-Button",
  props: ["text", "activeColor"],
};
</script>

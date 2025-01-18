<template>
  <button
    class="warning-button"
    :disabled="disabled"
  >
    {{ label }}
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'WarningButton',
  props: {
    label: {
      type: String,
      required: true,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
});
</script>

<style scoped>
.warning-button {
  background-color: #fcaa4c;
  border-radius: 100px;
  color: white;
  font-size: 14px;
  font-weight: 500;
  height: 36px;
  padding: 0 24px;
}
.warning-button:disabled {
  background-color: #d3d3d3;
  color: #888;
  cursor: not-allowed;
  box-shadow: none;
}
</style>
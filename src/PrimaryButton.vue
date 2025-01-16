<template>
  <button
    class="primary-button"
    :disabled="disabled"
  >
    {{ label }}
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PrimaryButton',
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
})
</script>

<style scoped>
.primary-button {
  background-color: #4c83fc;
  border-radius: 100px;
  color: white;
  font-size: 14px;
  font-weight: 500;
  height: 40px;
  padding: 8px 24px;
}
.primary-button:disabled {
  background-color: #d3d3d3;
  color: #888;
  cursor: not-allowed;
  box-shadow: none;
}
</style>
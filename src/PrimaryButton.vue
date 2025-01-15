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
  /* border: 1px solid rgba(32, 4, 175, 0.75); */
  /* box-shadow: 0 3px 6px rgba(199, 199, 199, 0.7); */
  color: white;
  font-size: 12px;
  font-weight: 600;
  height: 40px;
  /* padding:  0 0.938rem; */
  padding: 10px 24px;
  /* transition: background-color 0.3s ease, box-shadow 0.3s ease; */
}
/* .primary-button:hover {
  background-color: #0364cb;
  box-shadow: 0 3px 6px rgba(9, 113, 199, 0.8);
}
.primary-button:active {
  background-color: #004a9e;
  box-shadow: 0 2px 4px rgba(9, 106, 186, 0.9);
  transform: scale(0.98);
}
.primary-button:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(9, 106, 186, 0.5);
} */
.primary-button:disabled {
  background-color: #d3d3d3;
  color: #888;
  cursor: not-allowed;
  box-shadow: none;
}
</style>
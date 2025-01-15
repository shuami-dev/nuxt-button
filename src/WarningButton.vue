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
  /* border: 1px solid rgba(173, 130, 0, 0.75); */
  /* box-shadow: 0 3px 6px rgba(199, 199, 199, 0.7); */
  color: black;
  font-size: 12px;
  font-weight: 600;
  height: 40px;
  padding:  0 0.938rem;
  /* transition: background-color 0.3s ease, box-shadow 0.3s ease; */
}
/* .warning-button:hover {
  background-color: rgb(255, 193, 7);
  box-shadow: 0 3px 6px rgba(147, 123, 2, 0.7);
}
.warning-button:active {
  background-color: rgb(251, 140, 0);
  box-shadow: 0 2px 4px rgba(253, 224, 71, 0.9);
  transform: scale(0.98);
}
.warning-button:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(255, 193, 7, 0.5);
} */
.warning-button:disabled {
  background-color: #d3d3d3;
  color: #888;
  cursor: not-allowed;
  box-shadow: none;
}
</style>
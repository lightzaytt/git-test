<template>
  <button
    :type="type"
    class="button"
    :class="{ primary: color === 'primary', reverse, disabled }"
    :disabled="disabled"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    type: { type: String, default: "button" },
    color: {
      type: String,
      default: "primary",
    },
    reverse: Boolean,
    disabled: Boolean,
  },
};
</script>

<style scoped>
.button {
  border-radius: 8px;
  padding: 10px 32px;
  border: none;
  color: white;
  font-size: 16px;
}

.button.primary {
  background: #1da0ff;
}

.button.reverse {
  background: none;
  border: 1px solid #e8e8e8;
  color: initial;
}

.button.disabled {
  background-color: #d3d3d3;
  color: #a1a1a1;
  border: 1px solid #e0e0e0;
  cursor: not-allowed;
}
</style>

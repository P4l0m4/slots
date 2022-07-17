<template>
  <button
    class="p-button"
    :class="{ 'p-button--primary': primary, 'p-button--secondary': secondary, 'p-button--tertiary': tertiary }"
  >
    <slot name="left"></slot>
    {{ label }}
    <slot name="right"></slot>
  </button>
</template>
<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    primary: {
      type: Boolean,
      required: false,
      default: false,
    },
    secondary: {
      type: Boolean,
      required: false,
      default: false,
    },
    tertiary: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
}
</script>
<style lang="scss" scoped>
$color: orange;
.p-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 40px;
  padding: 0 1rem;

  &--primary {
    border: 1px solid $color;
    color: white;
    background-color: $color;
  }

  &--secondary {
    border: 1px solid $color;
    color: $color;
    background-color: transparent;
  }

  &--tertiary {
    color: $color;
  }
}
</style>

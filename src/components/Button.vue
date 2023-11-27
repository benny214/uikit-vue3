<template>
  <button :class="[
  'btn', 
  `btn--${color}`, 
  {'btn--rounded': rounded},
  {'btn--outlined': outlined}
  ]"
  :disabled="disabled">
    {{ label }}
  </button>
</template>
<script setup>
const props = defineProps({
  label: {
    type: String,
    default: "Button",
  },
  color: {
    type: String,
    default: "primary",
  },
  rounded: {
    type: Boolean,
    required: false,
  },
  disabled: {
    type: Boolean,
    required: false,
  },
  outlined: {
    type: Boolean,
    required: false
  }
});
</script>
<style lang="scss" scoped>
@import "@/assets/styles/main";
.btn {
  margin-right: 10px;
  margin-bottom: 10px;
  padding: 0 20px;
  height: 40px;
  color: #fff;
  border-radius: 7px;
  border: none;
  cursor: pointer;
  font-size: 15px;
  transition: 0.2s;
  &--primary {
    background-color: $primary;
    border: 1px solid $primary;
    &:enabled:hover {
      background-color: $primary-h;
      border-color: $primary-h;
    }
  }
  &--secondary {
    background-color: $secondary;
    border: 1px solid $secondary;
    &:enabled:hover {
      background-color: $secondary-h;
      border-color: $secondary-h;
    }
  }
  &--success {
    background-color: $success;
    border: 1px solid $success;
    &:enabled:hover {
      background-color: $success-h;
      border-color: $success-h;
    }
  }
  &--info {
    background-color: $info;
    border: 1px solid $info;
    &:enabled:hover {
      background-color: $info-h;
      border-color: $info-h;
    }
  }
  &--warning {
    background-color: $warning;
    border: 1px solid $warning;
    &:enabled:hover {
      background-color: $warning-h;
      border-color: $warning-h;
    }
  }
  &--danger {
    background-color: $danger;
    border: 1px solid $danger;
    &:enabled:hover {
      background-color: $danger-h;
      border-color: $danger-h;
    }
  }

  &--rounded {
    border-radius: 15px;
  }

  &:disabled {
    opacity: .6;
    cursor: default;
    &:hover {
      opacity: .6;
    }
  }

  &--outlined {
    background-color: transparent;
    color: #000;
    &:hover {
      color: #fff;
    }
  }
}
</style>

<template>
  <button :class="[
  'btn', 
  `btn--${color}`, 
  {'btn--rounded': rounded},
  {'btn--outlined': outlined},
  {'btn--icon': icon},
  {'btn--large': size === 'large'}
  ]"
  :disabled="disabled"
  @click="clickOnBtn">
    <span v-if="icon"><font-awesome-icon :icon="`fa-regular fa-${icon}`"/></span>
    <span v-else>{{ label }}</span> 
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
  },
  icon: {
    type: String,
    required: false
  },
  size: {
    type: String,
    default: 'normal'
  }
});

const emit = defineEmits(['click'])

const clickOnBtn = () => {
  emit('click')
}
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
  transition: .2s;
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

  &--icon {
    padding: 0;
    width: 40px;
    height: 40px;
    border-radius: 50%;
  }

  &--large {
    height: 48px;
    padding: 0 30px;
  }
}
</style>

<template>
  <h1 class="heading-1">Button</h1>
  <h2 class="heading-2">Colors</h2>
  <div class="line">
    <Button label="Primary" color="primary" />
    <Button label="Secondary" color="secondary" />
    <Button label="Success" color="success" />
    <Button label="Info" color="info" />
    <Button label="Warning" color="warning" />
    <Button label="Danger" color="danger" />
  </div>

  <h2 class="heading-2">Rounded</h2>
  <div class="line">
    <Button label="Primary" color="primary" rounded />
    <Button label="Secondary" color="secondary" rounded />
    <Button label="Success" color="success" rounded />
    <Button label="Info" color="info" rounded />
    <Button label="Warning" color="warning" rounded />
    <Button label="Danger" color="danger" rounded />
  </div>

  <h2 class="heading-2">Disabled</h2>
  <div class="line">
    <Button label="Primary" color="primary" disabled />
    <Button label="Secondary" color="secondary" disabled />
  </div>

  <h2 class="heading-2">Outlined</h2>
  <div class="line">
    <Button label="Primary" color="primary" outlined />
    <Button label="Secondary" color="secondary" outlined />
    <Button label="Success" color="success" outlined />
    <Button label="Info" color="info" outlined />
    <Button label="Warning" color="warning" outlined />
    <Button label="Danger" color="danger" outlined />
  </div>

  <h2 class="heading-2">Icons</h2>
  <div class="line">
    <Button icon="heart" color="primary" />
    <Button icon="hand" color="secondary" outlined />
    <Button icon="address-book" color="success" />
    <Button icon="credit-card" color="info" outlined />
    <Button icon="lemon" color="warning" />
    <Button icon="hourglass" color="danger" outlined />
  </div>

  <h2 class="heading-2">Size</h2>
  <div class="line">
    <Button label="Normal" color="primary" />
    <Button label="Large" color="secondary" size="large" />
  </div>

  <h2 class="heading-2">Event</h2>
  <div class="line">
    <Button label="Normal" color="primary" @click="eventForBtn" />
  </div>
</template>
<script setup>
import Button from "@/components/Button.vue";

const eventForBtn = () => {
  alert("You clicked btn");
};
</script>
<style lang="scss" scoped>
</style>

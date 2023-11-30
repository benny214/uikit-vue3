<template>
  <h1 class="heading-1">Checkbox</h1>
  <h2 class="heading-2">Checkbox Active</h2>
  {{ checkboxActive }}
  <div class="line">
    <Checkbox
      label="Checkbox Active"
      id="checkboxActive"
      name="checkboxActive"
      value="checkboxActive"
      v-model:checked="checkboxActive"
    />
  </div>

  <h2 class="heading-2">Checkbox Disabled</h2>
  <div class="line">
    <Checkbox
      label="Checkbox Disabled"
      id="checkboxDisabled"
      name="checkboxDisabled"
      value="checkboxDisabled"
      :disabled="checkboxDisabled"
      v-model:checked="checkboxDisabledChecked"
    />
  </div>

  <h2 class="heading-2">Checkbox Group</h2>
  <div class="line--block">
    <p>Selected Heroes: {{ selectedHeroes }}</p>
    <CheckboxGroup v-model:value="selectedHeroes" name="heroes" :options="listOfHeroes"/>
  </div>
</template>
<script setup>
import { ref } from "vue";
import Checkbox from "@/components/Checkbox/Checkbox.vue";
import CheckboxGroup from "@/components/Checkbox/CheckboxGroup.vue";

const checkboxActive = ref(true);
const checkboxDisabled = ref(true);
const checkboxDisabledChecked = ref(true)

const listOfHeroes = ref([
  {name: 'Spider Man', id: 'h1'},
  {name: 'Iron Man', id: 'h2'},
  {name: 'Hulk', id: 'h3'},
  {name: 'Thor', id: 'h4'},
  {name: 'Groot', id: 'h5'},
])
const selectedHeroes = ref([])
</script>
<style lang="scss" scoped></style>

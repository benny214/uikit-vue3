<template>
  <h1 class="heading-1">Radiobuttton</h1>
  <h2 class="heading-2">Basic</h2>
  <div class="line--block">
    <p>Selected club: {{ selectedClub }}</p>
    <div 
      v-for="club in footballClubs" 
      :key="club.id">
      <Radiobutton 
        :value="club.name"
        :label="club.name"
        :id="club.id"
        name="club"
        v-model:checked="selectedClub"/>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue"
import Radiobutton from "@/components/Radiobutton.vue"

const footballClubs = ref([
  {name: 'CSKA Moscow', id:'f1'},
  {name: 'Spartak Moscow', id:'f2'},
  {name: 'Dynamo Moscow', id:'f3'},
  {name: 'Lokomotiv Moscow', id:'f4'},
])

const selectedClub = ref({})
</script>
<style lang="scss" scoped>
@import "@/assets/styles/main";
</style>

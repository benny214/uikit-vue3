<template>
  <h1 class="heading-1">Progress</h1>
  <h2 class="heading-2">Progress bar</h2>
  <div class="line--block">
    <ProgressBar maxWidth="400px" :percent="percentBar" color="success"/>
    <div class="line">
      <Button label="ádd 10%" @click="addPercentBar"/>
      <Button label="reduce 10%" @click="reducePercentBar"/>
    </div>
    
  </div>
  
</template>
<script setup>
import {ref} from 'vue'
import ProgressBar from '@/components/Progress/ProgressBar.vue';
import Button from '@/components/Button.vue';

const percentBar = ref(10)

const addPercentBar = () => {
  percentBar.value += 10

  if (percentBar.value > 100) {
    percentBar.value = 100
  }
}

const reducePercentBar = () => {
  percentBar.value -= 10

  if (percentBar.value < 0) {
    percentBar.value = 0
  }
}
</script>
<style lang="scss" scoped>
  
</style>
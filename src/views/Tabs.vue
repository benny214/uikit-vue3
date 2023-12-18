<template>
  <h1 class="heading-1">Tabs</h1>
  <Tabs
    :names="tabs"
    :selectedTab="selectedTab"
    @changeTab="changeTab">
    <div v-if="selectedTab === 'First'">Lorem ipsum dolor sit amet.</div>
    <div v-if="selectedTab === 'Second'">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Esse ex iusto repellendus magni illo, tempora at ipsum eligendi voluptatibus! Vero.</div>
    <div v-if="selectedTab === 'Third'">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Et maiores excepturi velit nemo ab quaerat laboriosam ullam cum consequuntur, accusantium laborum quibusdam illo culpa blanditiis, alias sunt tenetur? Nesciunt ab libero culpa accusantium modi qui voluptas! Consequuntur quisquam voluptatum esse?</div>
    
  </Tabs>
</template>
<script setup>
import {ref} from 'vue'
import Tabs from '@/components/Tabs.vue'

const tabs = [
  {name: 'First', label: 'Lorem5'},
  {name: 'Second', label: 'Lorem20'},
  {name: 'Third', label: 'Lorem40'},
]

const selectedTab = ref('Second')

const changeTab = (tabName) => {
  selectedTab.value = tabName
}
</script>
<style lang="scss" scoped>
  
</style>
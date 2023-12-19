<template>
  <h1 class="heading-1">Table</h1>

  <BaseTable
    :head="tableHeads"
    :columnTemplates="tableSizeColumns">
  </BaseTable>
</template>
<script setup>
import BaseTable from '@/components/Table/BaseTable.vue'

const tableHeads = ['Id', 'Author', 'Title', 'Cover', '']
const tableSizeColumns = '50px 1fr 2fr 150px 140px'
</script>
<style lang="scss" scoped>
  
</style>
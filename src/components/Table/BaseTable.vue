<template>
  <div class="table__wrap">
    <div class="table">
      <div 
        class="table__head"
        :style="{'grid-template-columns': columnTemplates}">
        <div 
          class="table__head-name" 
          v-for="(element, i) of head" 
          :key="i">
          {{ element }}
        </div>
      </div>
      <slot></slot>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  head: {
    type: Array,
    required: false
  },
  columnTemplates: {
    type: String,
    required: false
  }
})
</script>
<style lang="scss" scoped>
.table {
  background-color: #fff;
  width: 100%;
  margin-bottom: 40px;
  margin-top: 15px;
  &__wrap {
    display: flex;
    justify-content: center;
  }
  &__head {
    padding: 5px 16px;
    display: grid;
    column-gap: 10px;
    align-items: center;
    border-bottom: 2px solid #eeeff4;
    background: #fff;
    &-name {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      color: #999;
      cursor: pointer;
    }
    @media screen and (max-width: 767px) {
      display: none;
    }
  }
}
</style>

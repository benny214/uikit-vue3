<template>
  <div class="container">
    <div @click="toggleMenu" :class="['sidebar-toggle', {'sidebar-toggle--opened': isOpenMenu}]">&#5125;</div>
    <LayoutHeader/>
    <LayoutSidebar :openSidebar="isOpenMenu"/>
    <div :class="['content', {'content--full': !isOpenMenu}]">
      <RouterView />
    </div>
  </div>
</template>

<script setup>
import LayoutHeader from '@/components/layout/Header.vue'
import LayoutSidebar from '@/components/layout/Sidebar.vue'
import { ref } from 'vue'

const isOpenMenu = ref(false)

const toggleMenu = () => {
  isOpenMenu.value = !isOpenMenu.value
}
</script>

<style scoped lang="scss">
@import 'assets/styles/main';

.content {
  max-width: 1400px;
  margin-top: 62px;
  margin-left: 250px;
  padding: 30px;
  transition: .2s;
  &--full {
    margin-left: 0;
  }
}

.sidebar-toggle {
  position: fixed;
  left: 0;
  width: 15px;
  background-color: $primary;
  height: 100%;
  top: 62px;
  z-index: 1;
  cursor: pointer;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
}

@media screen and (max-width: 1023px) {
  .content {
    margin-left: 0;
  }
}
</style>

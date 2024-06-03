<script setup>
import LayoutHeader from '@/components/layout/Header.vue';
import LayoutSidebar from '@/components/layout/Sidebar.vue';
</script>

<template>
  <div class="container">
    <LayoutHeader />
    <LayoutSidebar />
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<style lang="scss">
@import './styles/global.scss';

.content {
  margin-left: 250px;
  padding: 30px;
  max-width: 1400px;
  transition: 0.2s;

  &_full {
    margin-left: 0;
  }
}
</style>

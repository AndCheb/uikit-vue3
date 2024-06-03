<script setup>
import { ref } from 'vue';

const links = ref([
  {
    name: 'Typography',
    href: './typography',
  },
  {
    name: 'Button',
    href: './button',
  }
]);
</script>

<template>
  <div class="sidebar">
    <router-link
      class="sidebar__link"
      v-for="link in links" 
      :key="link.name"
      :to="link.href"
    >
      {{ link.name }}
    </router-link>
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  position: fixed;
  top: 62px;
  left: 0;
  padding: 20px;
  width: 250px;
  height: 100%;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.07);
  transform: translateX(0px);
  transition: 0.2s;

  &__link {
    display: block;
    margin-bottom: 10px;
    padding: 10px;
    font-weight: 700;
    border: 2px solid #fff;
    border-radius: 12px;
    transition: 0.2s;

    &:hover {
      border-color: var(--primary-color);
    }
  }
}
</style>
<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <Nav />

  <RouterView />
</template>

<script lang="ts">
import Nav from '@/components/Nav.vue';
export default {
  components: {
    Nav,
  },
}
</script>

<style>
html,
body {
  height: 100%;
}

.form-signin {
  max-width: 330px;
  padding: 1rem;
}

.form-signin .form-floating:focus-within {
  z-index: 2;
}

.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.form-signin input[type="password"] {
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
</style>
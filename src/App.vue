<template>
  <div class="container mx-auto p-4">
    <Header />
    <TaskList />
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import TaskList from './components/TaskList.vue';
import Footer from './components/Footer.vue';
</script>

<style scoped>
.container {
  max-width: 800px;
}
</style>
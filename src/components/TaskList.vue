<template>
  <div class="bg-white p-4 rounded-md shadow-md">
    <h2 class="text-lg font-semibold mb-2">Today's Tasks</h2>
    <ul>
      <li v-for="task in tasks" :key="task.id" class="flex justify-between items-center">
        <span>{{ task.name }}</span>
        <button class="bg-green-500 text-white px-2 py-1 rounded" @click="completeTask(task.id)">Complete</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const tasks = ref([
  { id: 1, name: 'Clean the kitchen' },
  { id: 2, name: 'Mow the lawn' },
  { id: 3, name: 'Do the laundry' }
]);

function completeTask(id) {
  tasks.value = tasks.value.filter(task => task.id !== id);
}
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li + li {
  margin-top: 0.5rem;
}
</style>
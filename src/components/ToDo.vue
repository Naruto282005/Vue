<template>
    <div v-if="tasks.length === 0" class="text-gray-500">No pending tasks.</div>
  
    <ul v-else>
      <li v-for="task in tasks" :key="task.id" class="mb-1">
        <span :class="{ 'line-through  ': task.completed }">
          {{ task.title }}
        </span>
      </li>
    </ul>
  
    //Computed Properties
    <div>
      <p>Completed: {{ completedTasks }}</p>
      <p>Pending: {{ pendingTasks }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue'
  
  //Array
  const tasks = ref([
    { id: 1, title: 'Buy Food.', completed: true },
    { id: 2, title: 'Eat the Food.', completed: true },
    { id: 3, title: 'Take a walk.', completed: false }
  ])
  
  //Computed Property
  const completedTasks = computed(() => tasks.value.filter((t) => t.completed).length)
  const pendingTasks = computed(() => tasks.value.filter((t) => !t.completed).length)
  </script>
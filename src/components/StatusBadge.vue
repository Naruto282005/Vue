<template>
    <span :class="badgeClass">
      {{ isActive ? 'Active' : 'Inactive' }}
    </span>
  </template>
  
  <script>
  export default {
    name: 'StatusBadge',
    props: {
      isActive: {
        type: Boolean,
        required: true
      }
    },
    computed: {
      badgeClass() {
        return this.isActive ? 'text-green-600 font-semibold' : 'text-gray-500 font-semibold';
      }
    }
  }
  </script>
  
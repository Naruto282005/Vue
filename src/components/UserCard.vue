<template>
    <div :class="cardClass" class="p-4 rounded-lg shadow-md">
      <h2 class="text-lg font-bold">{{ name }}</h2>
      <p>Age: {{ age }}</p>
      <p>Hobby: {{ hobby }}</p>
      <StatusBadge :isActive="isActive" />
    </div>
  </template>
  
  <script>
  import StatusBadge from './StatusBadge.vue';
  
  export default {
    name: 'UserCard',
    components: {
      StatusBadge
    },
    props: {
      name: {
        type: String,
        required: true
      },
      age: {
        type: Number,
        required: true
      },
      isActive: {
        type: Boolean,
        required: true
      },
      hobby: {
        type: String,
        required: true
      }
    },
    computed: {
      cardClass() {
        return {
          'border-2': true,
          'border-green-500': this.isActive,
          'border-red-500': !this.isActive,
          'bg-yellow-100': this.age < 27
        };
      }
    }
  }
  </script>
  
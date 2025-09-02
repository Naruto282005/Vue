<template>
  <span :class="badgeClass">{{ statusText }}</span>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  isActive: {
    type: Boolean,
    required: true,
  },
});

const statusText = computed(() => (props.isActive ? 'Active' : 'Inactive'));
const badgeClass = computed(() => (props.isActive ? 'active-badge' : 'inactive-badge'));
</script>

<style scoped>
.active-badge {
  color: green;
  font-weight: bold;
}

.inactive-badge {
  color: red;
}
</style>
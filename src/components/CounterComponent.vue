<template>
    <button @click="increment">{{ count }}</button>
</template>

<script setup> 
import { ref } from 'vue';


const emit = defineEmits([ 'updateCount']);
const coount = ref(0);

function increment() {
    count.value++;
    emit('updateCount', count.value);
}
</script>
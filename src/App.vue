<template>
  <div class="max-w-lg mx-auto mt-10 space-y-4">
    <UserCard
      v-for="(user, index) in users"
      :key="index"
      :name="user.name"
      :age="user.age"
      :isActive="user.isActive"
      :hobby="user.hobby"
    />
  </div>
</template>

<script>
import UserCard from './components/UserCard.vue';

export default {
  name: 'App',
  components: {
    UserCard
  },
  data() {
    return {
      users: [
        { name: 'Alice', age: 25, isActive: true, hobby: 'Reading' },
        { name: 'Bob', age: 30, isActive: false, hobby: 'Cycling' },
        { name: 'Charlie', age: 22, isActive: true, hobby: 'Gaming' }
      ]
    };
  }
}
</script>

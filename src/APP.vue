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
        { name: 'Bob', age: 30, isActive: true, hobby: 'Cycling' },
        { name: 'Charlie', age: 22, isActive: true, hobby: 'Gaming' },
        { name: 'Godzila', age: 31, isActive: true, hobby: 'Eating Humans' },
        { name: 'Guko', age: 19, isActive: true, hobby: 'Super Saiyan' }
      ]
    };
  }
}
</script>
<style>
  body {
    font-family: Arial, sans-serif;
    background-color: #861b1b;
  }
  .container {
    width: 80%;
    margin: 0 auto;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  h2 {
    color: #ffffff;
  }
  h2 {
    color: #fff;
  }
  p {
    color: #dfd9d9; /* A lighter gray for the details */
  }
</style>

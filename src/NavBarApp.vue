<template>
    <div>
      <NavBar />
      <h1>Hello World</h1>
      <div>
        <button class="btn btn-primary">Hit Me</button>
      </div>
    </div>
  </template>
  
  <script>
  import NavBar from "./components/NavBar.vue";
  
  export default {
    components: {
      NavBar,
    },
  };
  </script>
  
<template>
    <section class="profile">
      <h2>{{ name }}</h2>
      <p>{{ bio }}</p>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Profile',
    data() {
      return {
        name: 'Swandaru tirta sandhika',
        bio: 'Student Undergraduate Information Technology.',
      };
    },
  };
  </script>
  
  <style scoped>
  .profile {
    text-align: center;
    margin: 20px;
  }
  </style>
  
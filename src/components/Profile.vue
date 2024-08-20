<template>
    <section class="profile">
      <img :src="photo" alt="Student Photo" class="profile-photo"/>
      <h2>{{ name }}</h2>
      <p>{{ bio }}</p>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Profile',
    data() {
      return {
        name: 'John Doe',
        bio: 'A passionate student learning web development.',
        photo: '/src/assets/student-photo.jpg' // Ganti dengan path gambar yang sesuai
      };
    },
  };
  </script>
  
  <style scoped>
  .profile {
    text-align: center;
    margin: 20px;
  }
  .profile-photo {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 15px;
  }
  </style>
  
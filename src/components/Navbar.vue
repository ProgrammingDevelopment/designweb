<template>
  <nav class="navbar">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About Us</router-link></li>
      <li><router-link to="/events">Events</router-link></li>
      <li><router-link to="/contact">Contact Us</router-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style scoped>
.navbar {
  background-color: #2c3e50;
  color: #ecf0f1;
  padding: 10px 20px;
}

ul {
  display: flex;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  margin-right: 20px;
}

a {
  color: #ecf0f1;
  text-decoration: none;
  font-size: 18px;
}

a:hover {
  text-decoration: underline;
}
</style>

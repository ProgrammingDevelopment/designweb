<template>
  <div id="app">
    <Navbar />
    <router-view />
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-logo">
            <img src="./assets/your-logo.png" alt="Logo" class="logo" />
            <h1>Welcome, IT Class of 2024!</h1>
          </div>
          <div class="footer-links">
            <router-link to="/about">About Us</router-link>
            <router-link to="/events">Events</router-link>
            <router-link to="/resources">Resources</router-link>
            <router-link to="/contact">Contact Us</router-link>
          </div>
          <div class="footer-social">
            <a href="https://www.facebook.com" target="_blank">Facebook</a>
            <a href="https://www.twitter.com" target="_blank">Twitter</a>
            <a href="https://www.instagram.com" target="_blank">Instagram</a>
            <a href="https://www.linkedin.com" target="_blank">LinkedIn</a>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; 2024 Information Technology Department. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    Navbar,
  },
};
</script>

<style>
/* Global styles here, if needed */
</style>

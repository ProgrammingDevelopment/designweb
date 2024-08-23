<template>
  <div id="app">
    <Navbar />
    <router-view />
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-links">
            <router-link to="/about">About Us</router-link>
            <router-link to="/events">Events</router-link>
            <router-link to="/resources">Resources</router-link>
            <router-link to="/contact">Contact Us</router-link>
          </div>
          <div class="footer-social">
            <a href="https://www.facebook.com" target="_blank"><i class="fab fa-facebook-f"></i></a>
            <a href="https://www.twitter.com" target="_blank"><i class="fab fa-twitter"></i></a>
            <a href="https://www.instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://www.linkedin.com" target="_blank"><i class="fab fa-linkedin-in"></i></a>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; Divisi Penelitian & Pengembangan UBSI. All rights reserved.</p>
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

<style scoped>
/* Footer Styles */
.footer {
  background: linear-gradient(135deg, #ff7e5f, #feb47b, #ff6f91, #f7b42c);
  background-size: 400% 400%; /* To animate the gradient */
  color: #020202;
  padding: 30px 0;
  margin-top: 40px;
  animation: gradientAnimation 15s ease infinite;
}

@keyframes gradientAnimation {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.footer .container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1200px;
  margin-bottom: 20px;
}

.footer-links {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.footer-social {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.footer-links a,
.footer-social a {
  color: #4a03ff;
  text-decoration: none;
  font-weight: bold;
  position: relative;
  transition: color 0.3s ease, transform 0.3s ease;
}

.footer-links a:hover,
.footer-social a:hover {
  color: #000000;
  transform: scale(1.1);
}

.footer-links a::before,
.footer-social a::before {
  content: '';
  position: absolute;
  width: 0;
  height: 3px;
  background-color: #19b667;
  bottom: -5px;
  left: 50%;
  transform: translateX(-50%);
  transition: width 0.4s ease;
}

.footer-links a:hover::before,
.footer-social a:hover::before {
  width: 100%;
}

.footer-bottom {
  margin-top: 20px;
  color: #02142a;
}

.footer-social a {
  font-size: 24px;
  transition: transform 0.3s ease;
}

.footer-social a:hover {
  transform: scale(1.3);
}
</style>

<template>
  <div>
    <section class="home">
      <h1>Selamat datang Mahasiswa Teknologi Informasi UBSI</h1>
      <p>Kami dari Divisi Penelitian dan Pengembangan HMTI UBSI</p>

      <h3>Memperkenalkan Proyek kami: </h3>
      <p>Nama Proyek: Pengembangan Website HMTI</p>
      <p>Pengembang: Tim Divisi Penelitian & Pengembangan</p>

      <h3>Dokumentasi Proyek:</h3>
      <p>Ini adalah aplikasi web untuk organisasi mahasiswa, yang mencakup fitur-fitur seperti pengelolaan acara, profil organisasi, dan formulir kontak.</p>
    </section>

    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-logo">
            <img src="../assets/Logo BSI.png" alt="Logo" class="logo" />
            <h1>Selamat datang Di Teknologi Informasi!</h1>
          </div>
          <div class="footer-links">
            <a href="#about">About Us</a>
            <a href="#events">Events</a>
            <a href="#resources">Resources</a>
            <a href="#contact">Contact Us</a>
          </div>
          <div class="footer-social">
            <a href="https://www.facebook.com" target="_blank">Facebook</a>
            <a href="https://www.twitter.com" target="_blank">Twitter</a>
            <a href="https://www.instagram.com" target="_blank">Instagram</a>
            <a href="https://www.linkedin.com" target="_blank">LinkedIn</a>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; 2024 Reasearch & Development HMTI. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.home {
  text-align: center;
  padding: 50px 20px;
}

.home h1 {
  font-size: 36px;
  margin-bottom: 10px;
}

.home p {
  font-size: 18px;
  margin-bottom: 20px;
}

.footer {
  background-color: #2c3e50;
  color: #000000;
  padding: 20px 0;
  margin-top: 40px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.footer-logo {
  display: flex;
  align-items: center;
}

.logo {
  width: 50px;
  height: 50px;
  margin-right: 10px;
}

.footer-links a, .footer-social a {
  color: #000000;
  margin: 0 10px;
  text-decoration: none;
}

.footer-links a:hover, .footer-social a:hover {
  text-decoration: underline;
}

.footer-bottom {
  text-align: center;
  margin-top: 20px;
}
</style>

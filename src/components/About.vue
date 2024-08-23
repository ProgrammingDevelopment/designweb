<template>
  <div class="team-container">
    <h3>Tentang Kami</h3>
    <p>Kami adalah Tim dari Biro Teknologi Informasi HMTI kramat 98</p>
    <p>Pengembang: Tim Divisi Penelitian & Pengembangan</p>

    <h3>Dokumentasi Proyek:</h3>
    <p>Halaman ini memberikan informasi tentang organisasi mahasiswa, termasuk sejarah, visi, dan misi organisasi.</p>

    <h3>Tim Penelitian & Pengembangan HMTI UBSI:</h3>
    <div v-for="member in teamMembers" :key="member.name" class="team-member">
      <img :src="member.image" :alt="member.name">
      <div>
        <strong>Nama:</strong> {{ member.name }}<br>
        <strong>Jabatan:</strong> {{ member.position }}<br>
        <strong>Kontak:</strong> <a :href="member.contact" target="_blank">{{ member.contactText }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Team',
  data() {
    return {
      teamMembers: [
        {
          name: 'Swandaru Tirta Sandhika',
          position: 'Kepala Divisi',
          image: 'src/assets/swan.JPG',
          contact: 'https://www.linkedin.com/in/swandaru-tirta-sandhika/',
          contactText: 'LinkedIn', 
        },
        {
          name: 'Farid panji Alamsah',
          position: 'Anggota Divisi',
          image: 'src/assets/farid_anggota.JPG',
          contact: 'https://www.linkedin.com/in/farid-panji-alamsah',
          contactText: 'Linkedin'
        },
        {
          name: 'Sahira Bella Kintayari',
          position: 'Koordinator Proyek',
          image: 'src/assets/bella.JPG',
          contact: '',
          contactText: 'Email'
        },
        {
          name: 'Zay',
          position: 'Staff Muda Litbang',
          image: 'src/assets/Zay_staff.JPG',
          contact: '',
          contactText: 'GitHub'
        }
      ]
    };
  }
};
</script>

<style scoped>
.team-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.team-member {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
  padding: 10px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.team-member img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-right: 15px;
  object-fit: cover;
}

.team-member strong {
  display: block;
}
</style>

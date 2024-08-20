<template>
    <section class="events">
      <h2>Upcoming Events</h2>
      <ul>
        <li v-for="event in events" :key="event.id">
          <strong>{{ event.name }}</strong> - {{ event.date }}
        </li>
      </ul>
      <h3>Identitas Proyek:</h3>
      <p>Nama Proyek: Student Organization Web</p>
      <p>Pengembang: John Smith</p>
  
      <h3>Dokumentasi Proyek:</h3>
      <p>Halaman ini berisi daftar acara mendatang yang diselenggarakan oleh organisasi mahasiswa.</p>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Events',
    data() {
      return {
        events: [
          { id: 1, name: 'Orientation', date: 'September 1, 2024' },
          { id: 2, name: 'Hackathon', date: 'October 12, 2024' },
          { id: 3, name: 'Workshop on AI', date: 'November 23, 2024' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .events {
    padding: 20px;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    margin: 10px 0;
  }
  </style>
  
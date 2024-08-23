<template>
  <section class="events">
    <h2>Kegiatan Mendatang</h2>
    <ul>
      <li v-for="event in events" :key="event.id" class="event-item">
        <div class="event-details">
          <strong>{{ event.name }}</strong>
          <span class="event-date">{{ event.date }}</span>
        </div>
        <p class="event-description">{{ event.description }}</p>
      </li>
    </ul>
    <h3>Nama Venue:</h3>
    <p>Nama Proyek: Tournament Fun Match Mobile Legends</p>
    <p>Pengembang: HMTI UBSI</p>

    <h3>Dokumentasi Proyek:</h3>
    <p>Under Maintance!</p>
  </section>
</template>

<script>
export default {
  name: 'Events',
  data() {
    return {
      events: [], // Data akan diisi dengan data real-time
    };
  },
  async created() {
    await this.fetchEvents(); // Memanggil API untuk mendapatkan data acara
  },
  methods: {
    async fetchEvents() {
      try {
        const response = await fetch('https://api.example.com/events'); // Ganti dengan URL API Anda
        const data = await response.json();
        this.events = data.events; // Sesuaikan dengan struktur data API
      } catch (error) {
        console.error('Failed to fetch events:', error);
      }
    },
  },
};
</script>

<style scoped>
.events {
  padding: 20px;
  background-color: #f9f9f9;
}

h2 {
  font-size: 28px;
  margin-bottom: 20px;
}

ul {
  list-style-type: none;
  padding: 0;
}

.event-item {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 15px;
  padding: 15px;
  transition: background-color 0.3s;
}

.event-item:hover {
  background-color: #f1f1f1;
}

.event-details {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.event-date {
  color: #888;
}

.event-description {
  margin-top: 10px;
  color: #555;
}

h3 {
  font-size: 22px;
  margin-top: 30px;
}
</style>

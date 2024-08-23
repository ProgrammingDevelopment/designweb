<template>
    <section class="contact">
      <h2>Contact Us</h2>
      <form @submit.prevent="submitForm">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" required />
  
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required />
  
        <label for="message">Message:</label>
        <textarea id="message" v-model="message" required></textarea>
  
        <button type="submit">Submit</button>
      </form>
  
      <div v-if="messageSent" class="success-message">
        Your message has been sent successfully!
      </div>
    </section>
  </template>
  
  <script>
import emailjs from 'emailjs-com';

export default {
  name: 'Contact',
  data() {
    return {
      name: '',
      email: '',
      message: '',
      messageSent: false,
    };
  },
  methods: {
    async submitForm() {
      if (!this.name || !this.email || !this.message) {
        alert('Please fill out all fields before submitting the form.');
        return;
      }

      try {
        const templateParams = {
          name: this.name,
          email: this.email,
          message: this.message,
        };

        await emailjs.send(
          'service_5bmwtxt', // Service ID from Admin
          'template_okfo4ia', // Replace with your template ID
          templateParams,
          'iXO7_e9c6elpJjZjk' // Replace with your user ID (public key from Admin)
        );

        this.messageSent = true;
        this.name = '';
        this.email = '';
        this.message = '';
        alert('Pesan Berhasil Dikirim!');
      } catch (error) {
        console.error('Failed to send email:', error);
        alert('Failed to send message. Please try again later.');
      }
    },
  },
};
</script>


  
  <style scoped>
  .contact {
    padding: 20px;
  }
  form {
    display: flex;
    flex-direction: column;
  }
  label {
    margin: 10px 0 5px;
  }
  input,
  textarea {
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  button {
    padding: 10px 15px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  button:hover {
    background-color: #0056b3;
  }
  .success-message {
    color: green;
    margin-top: 20px;
  }
  </style>
  
<template>
    <section class="contact">
      <h2>Contact Us</h2>
      <form @submit.prevent="submitForm">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" />
  
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" />
  
        <label for="message">Message:</label>
        <textarea id="message" v-model="message"></textarea>
  
        <button type="submit">Submit</button>
      </form>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Contact',
    data() {
      return {
        name: '',
        email: '',
        message: '',
      };
    },
    methods: {
      submitForm() {
        alert(`Thank you, ${this.name}. We will contact you at ${this.email} soon.`);
        this.name = '';
        this.email = '';
        this.message = '';
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
  </style>
  
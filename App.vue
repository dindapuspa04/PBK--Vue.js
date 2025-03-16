<script setup>
import { ref } from 'vue';

// Reactive variable
const message = ref('Hello, Vue!');
const name = ref('Dinda Puspa');
const inputText = ref('');
const count = ref(0);
const isLoggedIn = ref(false);
</script>

<template>
  <div class="container">
    <h1>{{ message }}</h1>
    
    <!-- Text Interpolation -->
    <h2>Halo, {{ name }}!</h2>
    
    <!-- Form Binding -->
    <input v-model="inputText" placeholder="Ketik sesuatu..." class="input" />
    <p>Anda mengetik: <strong>{{ inputText }}</strong></p>
    
    <!-- Event Listener -->
    <button @click="count++" class="button">Tambah</button>
    <p>Nilai: <strong>{{ count }}</strong></p>
    
    <!-- Attribute Binding -->
    <a href="https://vuejs.org" target="_blank" class="link">Kunjungi Vue.js</a>
    
    <!-- Conditional Rendering -->
    <button @click="isLoggedIn = !isLoggedIn" class="button">{{ isLoggedIn ? 'Logout' : 'Login' }}</button>
    <p v-if="isLoggedIn">Anda sudah login.</p>
    <p v-else>Silakan login.</p>
  </div>
</template>

<style scoped>
.container {
  max-width: 600px;
  margin: 50px auto;
  text-align: center;
  font-family: 'Arial', sans-serif;
  background: #f8f9fa;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}
h1 {
  color: #343a40;
  font-size: 2.5rem;
  font-weight: bold;
}
h2 {
  color: #cb1485;
}
.input {
  padding: 10px;
  width: 80%;
  border: 2px solid #007bff;
  border-radius: 5px;
  margin: 10px 0;
}
.button {
  padding: 10px 20px;
  background: blue;
  color: white;
  border: none;
  cursor: pointer;
  font-size: 1rem;
  border-radius: 5px;
  margin: 10px;
  transition: 0.3s;
}
.button:hover {
  background: darkblue;
}
.link {
  display: block;
  margin: 10px 0;
  color: green;
  font-weight: bold;
  text-decoration: none;
  font-size: 1.2rem;
}
</style>

<template>
  <div class="login-page">
    <div class="card">
      <h2>Login</h2>
      <form @submit.prevent="handleLogin">
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" v-model="email" id="email" required />
        </div>
        <div class="form-group">
          <label for="password">Password:</label>
          <input type="password" v-model="password" id="password" required />
        </div>
        <button type="submit">Login</button>
      </form>
      <p>
        Not a member? <router-link to="/register">Register here</router-link>
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const email = ref('');
const password = ref('');
const router = useRouter();

const handleLogin = () => {
  console.log('Logging in:', email.value, password.value);
  // Handle login logic here (e.g., authentication, redirect)
  router.push('/dashboard'); // Example redirect after successful login
};
</script>

<style scoped>
html, body {
  height: 100%;
  margin: 0;
}

.login-page {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #ffffff; /* White background for the whole page */
}

.card {
  background: rgba(255, 255, 255, 0.1); /* Very light transparent gray */
  backdrop-filter: blur(15px); /* Glass effect */
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37); /* Soft shadow */
  border: 1px solid rgba(255, 255, 255, 0.3); /* Semi-transparent border */
  max-width: 400px;
  width: 100%;
  box-sizing: border-box;
}

h2 {
  margin-bottom: 20px;
  color: #333;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 5px;
}

button {
  width: 100%;
  padding: 10px;
  background-color: #1890ff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #40a9ff;
}

p {
  text-align: center;
  margin-top: 20px;
}
</style>


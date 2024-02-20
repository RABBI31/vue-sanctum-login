<template>
  <div>
    <form @submit.prevent="login">
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script setup>
import axios from 'axios';

const login = async () => {
  // await axios.get('/sanctum/csrf-cookie');
  await axios.post('/login', {
    email: 'test@example.com',
    password:'password'
  })
}
</script>

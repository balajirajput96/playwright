<template>
  <main>
    <h2>Login</h2>
    <form @submit.prevent="handleSubmit">
      <div>
        <label for="username">Username or email address</label>
        <input
          id="username"
          v-model="username"
          type="text"
          placeholder="Enter username"
        />
      </div>
      <div>
        <label for="password">Password</label>
        <input
          id="password"
          v-model="password"
          type="password"
          placeholder="Enter password"
        />
      </div>
      <button type="submit">Sign in</button>
    </form>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const username = ref('');
const password = ref('');

const handleSubmit = () => {
  console.log('Login attempted', { username: username.value, password: password.value });
};
</script>

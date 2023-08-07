<template>
    <main class="form-signin w-100 m-auto">
    <form @submit.prevent="submit">
      <h1 class="h3 mb-3 fw-normal">Register</h1>

      <div class="form-floating">
        <input v-model="data.first_name" class="form-control" placeholder="First name">
        <label>First name</label>
      </div>

      <div class="form-floating">
        <input v-model="data.last_name" class="form-control" placeholder="Last name">
        <label>Last name</label>
      </div>

      <div class="form-floating">
        <input v-model="data.email" type="email" class="form-control" placeholder="name@example.com">
        <label>Email address</label>
      </div>

      <div class="form-floating">
        <input v-model="data.password" type="password" class="form-control" placeholder="Password">
        <label>Password</label>
      </div>

      <div class="form-floating">
        <input v-model="data.password_confirm" type="password" class="form-control" placeholder="Confirm password">
        <label>Confirm password</label>
      </div>

      <button class="btn btn-primary w-100 py-2 mt-3" type="submit">Register</button>
    </form>
  </main>
</template>

<script lang="ts">
import { reactive } from 'vue';
import axios from 'axios';
import { useRouter } from 'vue-router';

export default {
  name: 'Register',
  setup() {
    const data = reactive({
      first_name: '',
      last_name: '',
      email: '',
      password: '',
      password_confirm: ''
    });

    const router = useRouter();

    const submit = async () => {
      await axios.post('http://localhost:8000/api/register', data);

      await router.push('/login');
    }

    return {
      data,
      submit
    }
  }
}
</script>
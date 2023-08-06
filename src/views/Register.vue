<template>
    <main class="form-signin w-100 m-auto">
    <form>
      <h1 class="h3 mb-3 fw-normal">Register</h1>

      <div class="form-floating">
        <input class="form-control" placeholder="First name">
        <label>First name</label>
      </div>

      <div class="form-floating">
        <input class="form-control" placeholder="Last name">
        <label>Last name</label>
      </div>

      <div class="form-floating">
        <input type="email" class="form-control" placeholder="name@example.com">
        <label>Email address</label>
      </div>

      <div class="form-floating">
        <input type="password" class="form-control" placeholder="Password">
        <label>Password</label>
      </div>

      <div class="form-floating">
        <input type="password" class="form-control" placeholder="Confirm password">
        <label>Confirm password</label>
      </div>

      <button class="btn btn-primary w-100 py-2 mt-3" type="submit">Register</button>
    </form>
  </main>
</template>

<script lang="ts">
export default {
  name: 'Register',
}
</script>
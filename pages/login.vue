<template>
  <section>
    <form>
      <h1>Login Page</h1>
      <div class="form-group">
        <input type="text" class="form-control">
      </div>
      <p>
        <nuxt-link no-prefetch to="/">Home</nuxt-link>
      </p>
      <button class="btn btn-primary" type="submit">Login</button>
    </form>
  </section>
</template>

<script>
export default {
  layout: 'empty'
}
</script>

<style scoped>
  form {
    width: 500px;
    margin: 0 auto;
  }
</style>

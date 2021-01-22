<template>
  <section>
    <h1>Users Page</h1>
    <ul>
      <li v-for="user of users" :key="user.id">
        <nuxt-link no-prefetch :to="'/users/' + user.id">{{user.name}}</nuxt-link>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  async fetch({ store }) {
    if(store.getters['users/users'].length === 0)
      await store.dispatch('users/fetch')
  },
  computed: {
    users() {
      return this.$store.getters['users/users']
    }
  }
}
</script>

<style lang="scss" scoped>

</style>

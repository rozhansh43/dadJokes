<template>
    <nuxt-link :to="'jokes/' + id">
      <b-card :title="joke" sub-title="Card subtitle">
        <nuxt-link :to="'jokes/' + id" class="card-link">
          read more
        </nuxt-link>
      </b-card>
    </nuxt-link>
</template>

<script>
export default {
  name: 'Joke',
  props: ["joke", "id"]
}
</script>

<style>
  a {
    text-decoration: none;
  }
</style>

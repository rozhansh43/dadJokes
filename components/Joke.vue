<template>
    <nuxt-link :to="'jokes/' + id">
      <p>
        {{ joke }}
      </p>
    </nuxt-link>
</template>

<script>
export default {
  name: 'Joke',
  props: ["joke", "id"]
}
</script>

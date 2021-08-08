<template>
  <b-form @submit.prevent="onSubmit" class="my-3">
    <b-input-group>
      <b-form-input type="text" v-model="text" placeholder="Search Jokes..."/>

      <b-input-group-append>
        <b-button type="submit" variant="primary">
          Search
        </b-button>
      </b-input-group-append>
    </b-input-group>
  </b-form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: ""
    }
  },
  methods: {
    onSubmit () {
      this.$emit ("search-text", this.text)
      this.text = ""
    }
  }
}
</script>

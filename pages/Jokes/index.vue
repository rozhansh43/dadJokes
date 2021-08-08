<template>
  <div>
     <SearchJokes @search-text="searchText"/>
      <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </div>
</template>

<script>
import axios from "axios"
import Joke from "@/components/Joke"
import SearchJokes from "@/components/SearchJokes"

export default {
  name:'Jokes',
  components: {
    Joke,
    SearchJokes
  },
  data () {
    return {
      jokes: [],

    }
  },
  async created () {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get ("https://icanhazdadjoke.com/search", config)
      this.jokes = res.data.results
    } catch (err) {
      console.log (err)
    }
  },
  methods: {
    async searchText (text) {
      const config = {
        headers: {
          Accept: "application/json"
        }
      };
      try {
        const res = await axios.get(
          `https://icanhazdadjoke.com/search?term=${text}`,
          config
        );
        this.jokes = res.data.results
      } catch (err) {
        console.log(err)
      }
    }
  },
  head () {
    return {
      title: "jokes list",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "jokes list content"
        }
      ]
    }
  }
}
</script>

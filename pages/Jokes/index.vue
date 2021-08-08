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
  async asyncData () {
    const config = {
      headers: {
        Accept: "application/json"
      }
    }
    try {
      let res = await axios.get ("https://icanhazdadjoke.com/search", config)
      return { jokes : res.data.results }
    } catch (error) {
      console.log (error)
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

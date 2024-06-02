<template>
  <br />
  <form>
    <label>Enter gif name</label>
    <input type="text" v-model="search" required /><br />
    <input type="button" value="Search" v-on:click="searchGif" />
  </form>
</template>

<script>
export default {
  name: "SwethaWelcome",
  data() {
    return {
      search: "vasu",
      searchResults: [],
    };
  },
  methods: {
    async searchGif() {
      
    },
  },
};
</script>

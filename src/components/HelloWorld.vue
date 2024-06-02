<template>
  <button v-on:click="getAnswer">Next</button>
  <h1>{{ info.answer }}</h1>
  <div v-if="info.answer === 'yes'">
    <img v-bind:src="info.image" alt="swetha" />
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      info: {},
    };
  },
  methods: {
    async getAnswer() {
      const { data } = await axios.get("https://yesno.wtf/api");
      this.info = data;
    },
  },
};
</script>



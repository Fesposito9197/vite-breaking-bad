<script>
import axios from "axios";
import CardCharacters from "./CardCharacters.vue";

export default {
  name: "AppCharacters",
  components: {
    CardCharacters,
  },
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.characters = resp.data;
    });
  },
};
</script>

<template>
  <div class="container pt-5 px-4">
    <h3 class="text-white p-2">Found 62 Characters</h3>
    <div class="container pb-5">
      <div class="row px-4 gy-3">
        <CardCharacters v-for="character in characters" :info="character" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  background-color: #fff;
  h3 {
    background-color: var(--my-secondary-color);
  }
}
</style>

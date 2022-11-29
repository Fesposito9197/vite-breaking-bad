<script>
import axios from "axios";
import { store } from "../store";
import AppSelect from "./AppSelect.vue";
import AppCharacters from "./AppCharacters.vue";

export default {
  name: "AppMain",
  components: {
    AppSelect,
    AppCharacters,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    searching() {
      axios
        .get("https://www.breakingbadapi.com/api/characters", {
          params: {
            category: this.store.category,
          },
        })
        .then((resp) => {
          this.store.characters = resp.data;
        });
    },
  },
  created() {
    this.searching();
  },
};
</script>

<template>
  <div class="container my-4">
    <AppSelect @search="searching" />
  </div>
  <div class="container">
    <AppCharacters />
  </div>
</template>

<style lang="scss" scoped></style>

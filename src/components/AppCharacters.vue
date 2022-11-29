<script>
import CardCharacters from "./CardCharacters.vue";
import { store } from "../store";

export default {
  name: "AppCharacters",
  components: {
    CardCharacters,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container bg-white pt-5 px-4">
    <h3 class="text-white p-2">
      Found {{ store.characters.length }} Characters
    </h3>
    <div class="container pb-5">
      <div class="row px-4 gy-3">
        <CardCharacters
          v-for="character in store.characters"
          :info="character"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
h3 {
  background-color: var(--my-secondary-color);
}
</style>

<script>
import AppSelect from "./AppSelect.vue";
import AppCharacters from "./AppCharacters.vue";

export default {
  name: "AppMain",
  components: {
    AppSelect,
    AppCharacters,
  },
};
</script>

<template>
  <div class="container my-4">
    <AppSelect />
  </div>
  <div class="container">
    <AppCharacters />
  </div>
</template>

<style lang="scss" scoped></style>

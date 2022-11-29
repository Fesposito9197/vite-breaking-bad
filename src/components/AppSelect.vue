<script>
import { store } from "../store";

export default {
  name: "AppSelect",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <select
    class="form-select w-auto"
    aria-label="Default select example"
    v-model="store.category"
    @change="$emit('search')"
  >
    <option disabled value="">Select Category</option>
    <option value="Breaking Bad">Breaking Bad</option>
    <option value="Better Call Saul">Better Call Saul</option>
  </select>
</template>

<style lang="scss" scoped></style>

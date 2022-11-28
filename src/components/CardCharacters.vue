<script>
export default {
  name: "CardCharacters",
  props: {
    info: Object,
  },
};
</script>

<template>
  <div class="card-container">
    <div class="my-card">
      <img class="img-fluid p-2" :src="info.img" :alt="info.name" />
      <h3 class="text-white text-center">{{ info.name }}</h3>
      <div class="series text-secondary text-center">{{ info.category }}</div>
      <div class="status text-secondary text-center">{{ info.status }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.my-card {
  background-color: var(--my-primary-color);
  height: 100%;
}
.series {
  margin-top: 20px;
}
.status {
  padding-bottom: 40px;
}
.card-container {
  width: calc((100% / 5));
  padding: 10px;
}
</style>

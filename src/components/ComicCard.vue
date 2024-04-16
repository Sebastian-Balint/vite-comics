<script>
export default {
  name: "ComicCard",
  props: ["chiave"],
};
</script>

<template>
  <div class="card">
    <div class="img-container">
      <img :src="chiave.thumb" alt="" />
    </div>
    <h3>{{ chiave.series }}</h3>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card {
  width: calc(100% / 6 - 24px);
  margin: 18px 8px;

  .img-container {
    width: 100%;
    aspect-ratio: 1;
    overflow: hidden;
    img {
      width: 100%;
      object-fit: cover;
    }
  }
  h3 {
    margin-top: 10px;
    font-size: 14px;
    text-transform: uppercase;
  }
}
</style>

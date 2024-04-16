<script>
export default {
  name: "AppJumbo",
  data() {
    return {};
  },
};
</script>

<template>
  <div class="container">
    <img src="../assets/img/jumbotron.jpg" alt="" />
    <div class="badge">CURRENT SERIES</div>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.container {
  position: relative;

  img {
    width: 100%;
    height: 300px;
    object-fit: cover;
    display: block;
    object-position: top;
  }
  .badge {
    position: absolute;
    left: 200px;
    bottom: -20px;
    padding: 10px 16px;
    background-color: $brand-primary;
    color: white;
    font-size: 24px;
  }
}
</style>

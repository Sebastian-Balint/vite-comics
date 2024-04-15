<script>
export default {
  name: "AppList",
  data() {
    return {};
  },
};
</script>

<template>
  <div class="container">
    <div class="container-info">
      <h1>-> Content goes here <-</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  background-color: black;
  width: 100%;
  height: 200px;
  .container-info {
    max-width: 1000px;
    margin: 0 auto;
    color: white;
    h1 {
      color: white;
      text-align: center;
      line-height: 200px;
    }
  }
}
</style>

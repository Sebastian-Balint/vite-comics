<script>
// JS
import AppHeader from "./components/AppHeader.vue";
import AppList from "./components/AppList.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AppInfo from "./components/AppInfo.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  components: {
    AppHeader,
    AppList,
    AppJumbo,
    AppInfo,
    AppFooter,
  },
};
</script>
<template>
  <!-- HTML -->
  <AppHeader></AppHeader>
  <main>
    <AppJumbo></AppJumbo>
    <AppList></AppList>
    <AppInfo></AppInfo>
  </main>
  <AppFooter></AppFooter>
</template>
<style lang="scss">
/* CSS */
@use "./style/generic";
</style>

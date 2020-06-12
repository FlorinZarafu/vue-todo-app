<template>
  <div id="app">
    <div id="nav">
      <Header />
      <router-view />
    </div>
  </div>
</template>

<script>
import Header from "./components/layouts/Header";
export default {
  name: "app",
  components: {
    Header,
  },
};
</script>

<style scoped></style>

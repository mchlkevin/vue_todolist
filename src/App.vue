<template>
  <Header />
  <router-view />
</template>

<script>
import Header from "./components/layout/Header.vue";
export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Barlow&display=swap");
* {
  font-family: "Barlow", sans-serif;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  font-size: 20px;
}

</style>

<template>
  <header class="header">
    <h1>To-do List</h1>
    <nav>
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li>|</li>
        <li><router-link to="/about">About</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "header-page",
};
</script>

<style scoped>
.header {
  background: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
}
.header a {
  color: #fff;
  padding: 5px;
  text-decoration: none;
}

ul>li{
  display: inline-block;
}
li{
  font-weight: bold;
}
</style>

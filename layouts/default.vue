<template>
  <div class="container">
    <AppHeader/>
    <Nuxt />

    <footer class="bawah">
      <p>&copy; 2021 maya</p>
    </footer>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";
export default {
  components: {
    AppHeader
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #f4f4f4;
}

a {
  color: #666;
  text-decoration: none;
}

ul {
  list-style: none;
}

.container {
  max-width: 900px;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}

.bawah {
  text-align: center;
  font-size: 0.75rem;
  padding: 1rem;
}
</style>

<template>
  <div id="app">
    <div class="body">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style lang="scss">
body {
  padding: 0;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-image: url("./assets/background.jpg");

  .body {
    padding: 1em;
  }

  *,
  *::after,
  *::before {
    -webkit-user-select: none;
    -webkit-user-drag: none;
    -webkit-app-region: no-drag;
    cursor: default;
  }
}
</style>

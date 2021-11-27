<template>
  <nav>
    <div class="content">
      <div class="title">Scrabble</div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Home",
  computed: {},
  components: {},
  methods: {},
};
</script>

<style scoped lang="scss">
nav {
  position: fixed;
  top: 0;
  z-index: 1;
  width: 100%;
  background-color: #212529;

  .content {
    margin: 0.25em 0.5em;
    display: flex;
    align-items: center;

    .title {
      padding: 10px;
      font-size: 14px;
      color: #ffffff;
      text-align: center;
    }

    .button-group {
      margin-left: auto;
    }
  }
}
</style>

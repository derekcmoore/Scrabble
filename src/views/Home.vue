<template>
  <div class="home">
    <Board />
    <CurrentHand />
  </div>
</template>

<script>
import Board from "../components/Board.vue";
import CurrentHand from "../components/CurrentHand.vue";

export default {
  name: "Home",
  computed: {},
  data() {
    return {};
  },
  components: {
    Board,
    CurrentHand,
  },
  created() {},
  methods: {},
};
</script>

<style scoped lang="scss"></style>

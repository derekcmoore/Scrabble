<template>
  <table>
    <tr v-for="(row, index1) in squares" :key="index1">
      <td v-for="(squareType, index2) in row" :key="`${index1}-${index2}`">
        <Square :type="squareType" />
      </td>
    </tr>
  </table>
</template>

<script>
import Square from "../components/Square.vue";

export default {
  name: "Board",
  computed: {},
  data() {
    return {
      squares: [
        [4, 0, 0, 1, 0, 0, 0, 4, 0, 0, 0, 1, 0, 0, 4],
        [0, 3, 0, 0, 0, 2, 0, 0, 0, 2, 0, 0, 0, 3, 0],
        [0, 0, 3, 0, 0, 0, 1, 0, 1, 0, 0, 0, 3, 0, 0],
        [1, 0, 0, 3, 0, 0, 0, 1, 0, 0, 0, 3, 0, 0, 1],
        [0, 0, 0, 0, 3, 0, 0, 0, 0, 0, 3, 0, 0, 0, 0],
        [0, 2, 0, 0, 0, 2, 0, 0, 0, 2, 0, 0, 0, 2, 0],
        [0, 0, 1, 0, 0, 0, 1, 0, 1, 0, 0, 0, 1, 0, 0],
        [4, 0, 0, 1, 0, 0, 0, 5, 0, 0, 0, 1, 0, 0, 4],
      ],
    };
  },
  components: {
    Square,
  },
  created() {
    this.flipBoard();
  },
  methods: {
    flipBoard() {
      let length = this.squares.length;
      for (let i = 2; i <= length + 1; i++) {
        this.squares.push(this.squares[length - i]);
      }
    },
  },
};
</script>

<style scoped lang="scss">
table {
  margin-left: auto;
  margin-right: auto;
  border-collapse: collapse;
  outline: 2px solid black;
}

tr,
td {
  padding: 0px;
}
</style>

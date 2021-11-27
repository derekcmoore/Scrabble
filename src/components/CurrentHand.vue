<template>
  <div class="hand">
    <table>
      <tr>
        <td v-for="i in 7" :key="`hand-${i}`">
          <span v-if="hand[i]">
            <Letters :letter="hand[i]" />
          </span>
          <input type="text" v-model="hand[i]" v-else />
        </td>
      </tr>
    </table>
    <div class="btn-group">
      <button class="btn btn-primary">set board</button>
    </div>
  </div>
</template>

<script>
import Letters from "./Letters.vue";

export default {
  name: "CurrentHand",
  computed: {},
  data() {
    return {
      hand: [],
    };
  },
  components: { Letters },
  methods: {},
};
</script>

<style scoped lang="scss">
.hand {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/background.jpg");
  background-position: center top;
  width: 100%;
  height: 60px;
  position: fixed;
  bottom: 0;
  right: 0;

  table {
    position: absolute;
    right: 50%;
    bottom: 10px;
    transform: translate(50%, 0%);
  }

  input {
    width: 30px;
    height: 30px;
    text-align: center;
    border: 1px solid #000000;
    border-radius: 4px;
  }

  .btn-group {
    float: right;
    margin: 15px;
  }
}
</style>

<template>
  <div class="square">
    <Letters :letter="value" v-if="value" />
    <input
      type="text"
      :class="types[type]"
      :placeholder="types[type]"
      v-model="value"
      v-else
    />
  </div>
</template>

<script>
import Letters from "./Letters.vue";

export default {
  name: "Square",
  props: {
    type: Number,
  },
  computed: {},
  data() {
    return {
      types: { 0: "", 1: "DL", 2: "TL", 3: "DW", 4: "TW", 5: "*" },
      value: null,
    };
  },
  components: { Letters },
  methods: {},
};
</script>

<style scoped lang="scss">
.square {
  height: auto;

  input {
    width: 30px;
    height: 30px;
    text-align: center;
    border: 1px solid #000000;

    &::placeholder {
      color: #ffffff;
    }

    &:placeholder-shown {
      font-weight: 600;

      &.DW {
        background-color: #5c4f8c;
      }

      &.TW {
        background-color: #bf639f;
      }

      &.DL {
        background-color: #2e2473;
      }

      &.TL {
        background-color: #5278b7;
      }
    }
    &:focus-visible {
      outline: none;
    }
  }
}
</style>

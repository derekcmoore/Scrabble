<template>
  <div class="tile">
    <div class="letter">{{ letter.charAt(0).toUpperCase() }}</div>
    <div class="value">{{ values[letter] }}</div>
  </div>
</template>

<script>
export default {
  name: "Letters",
  props: {
    letter: String,
  },
  data() {
    return {
      values: {
        a: 1,
        b: 3,
        c: 3,
        d: 2,
        e: 1,
        f: 4,
        g: 2,
        h: 4,
        i: 1,
        j: 8,
        k: 5,
        l: 1,
        m: 3,
        n: 1,
        o: 1,
        p: 3,
        q: 10,
        r: 1,
        s: 1,
        t: 1,
        u: 1,
        v: 4,
        w: 4,
        x: 8,
        y: 4,
        z: 10,
      },
    };
  },
  components: {},
  methods: {},
};
</script>

<style scoped lang="scss">
.tile {
  background-color: #ffe1b4;
  position: relative;
  width: 34px;
  height: 32px;
  border: 1px solid #dbb157;
  .letter {
    right: 50%;
    bottom: 50%;
    transform: translate(50%, 50%);
    position: absolute;
  }
  .value {
    position: absolute;
    right: 0;
    bottom: 0;
    font-size: 11px;
    margin: 2px 3px;
  }
}
</style>

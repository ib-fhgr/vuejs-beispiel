<template>
  <div>
    <span class="number">{{ number }}</span
    ><br />
    <button @click="up">Up</button><br />
    <button @click="reset">Reset</button>
  </div>
</template>

<script>
export default {
  name: "counter",
  data: function () {
    return {
      number: this.start,
    };
  },
  props: {
    start: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    up: function () {
      this.number++;
    },
    reset: function () {
      this.number = 0;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.number {
  font-weight: bold;
  font-size: 2em;
  color: red;
}
</style>

<template>
  <p>Reaction Time: {{ score }}ms</p>
  <h1>{{ rank }}</h1>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "So fast";
    } else if (this.score < 400) {
      this.rank = "Average";
    } else {
      this.rank = "So slow";
    }
  },
};
</script>

<style></style>

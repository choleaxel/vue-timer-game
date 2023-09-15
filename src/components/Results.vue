<template>
  <p>Reaction Time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
      this.rank = "Jedi";
    } else if (this.score < 400) {
      this.rank = "Padawan";
    } else {
      this.rank = "Stormtrooper";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: red;
  font-weight: bold;
}
</style>

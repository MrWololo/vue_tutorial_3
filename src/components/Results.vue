<template>
  <p>Reaction Time: {{ score }}</p>
  <h2 class="rank">{{ rank }}</h2>
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
    if (this.score < 50) {
      this.rank = "The fuck";
    } else if (this.score < 150) {
      this.rank = "Okay wow";
    } else if (this.score < 200) {
      this.rank = "Impressive";
    } else if (this.score < 250) {
      this.rank = "Gamer moment";
    } else if (this.score < 300) {
      this.rank = "Getting into slow territory";
    } else if (this.score < 400) {
      this.rank = "Go to sleep grandpa";
    } else {
      this.rank = "lol u alright?";
    }
  },
};
</script>

<style>
.rank {
  color: rgb(24, 197, 139);
  font-weight: bold;
}
</style>
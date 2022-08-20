<template>
  <div>
    <button @click="display_snake">Snake</button>
    <h3>{{ styled_joke }}</h3>
  </div>
</template>

<script>
export default {
//   data() {
//     return {
//       jokes: styled_joke,
//     };
//   },

  methods: {
    display_joke(jokes) {
      jokes;
    },
},

  mounted() {
    this.$root.$on(`style_joke`, this.display_joke);
  },
};
</script>

<style scoped>
</style>
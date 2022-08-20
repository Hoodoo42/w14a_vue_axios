<template>
  <div>
    <button>Normal</button>
  </div>
</template>

<script>
export default {
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
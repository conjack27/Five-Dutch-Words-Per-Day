<template>
  <div class="container">
    <h1 class="font-body text-6xl text-white text-center mt-24">Learn 5 Dutch words per day</h1>
    <app-cards />
  </div>
</template>

<script>
import cards from "~/components/cards.vue";

export default {
  name: "cards",
  components: {
    "app-cards": cards
  },
  data: () => ({}),
  methods: {}
};
</script>


<style>
</style>

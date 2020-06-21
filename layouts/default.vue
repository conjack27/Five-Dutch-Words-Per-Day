<template>
  <div class="custom-bg h-screen">
    <div class="container mx-auto">
      <app-navigation/>
      <nuxt />
    </div>
  </div>
</template>

<script>
import navigation from '~/components/navigation.vue'

export default {
  components: {
    'app-navigation': navigation
  }
}
</script>

<style>
.custom-bg {
  background-color: #FAACA8;
  background-image: linear-gradient(19deg, #FAACA8 0%, #DDD6F3 100%);
}
</style>

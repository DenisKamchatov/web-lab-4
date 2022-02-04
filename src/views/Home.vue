<template>
    <div class="text-center ma-10">
      <div class="text-h1 ">Добро пожаловать!</div>
      <div class="text-h3">
        Денис Камчатов, 201-321
      </div>
    <Slider />
    </div>
</template>

<script>
import Slider from '@/components/Slider.vue'

export default {
  name: "Home",
  components: {
      Slider
  },
};
</script>

<style>
</style>
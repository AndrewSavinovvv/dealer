<script setup>

import CategoriesComponent from "@/components/CategoriesComponent.vue";
import MainComponent from "@/components/MainComponent.vue";
import VariationsComponent from "@/components/VariationsComponent.vue";
import PopularComponent from "@/components/PopularComponent.vue";
</script>

<template>
  <MainComponent></MainComponent>
  <div class="container">
    <VariationsComponent></VariationsComponent>
    <PopularComponent></PopularComponent>
    <CategoriesComponent></CategoriesComponent>
  </div>
</template>

<style scoped>

</style>
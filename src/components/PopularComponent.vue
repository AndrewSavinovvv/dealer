<script setup>
import {  computed } from 'vue';
import CardComponent from '@/components/CardComponent.vue';

import item from "@/assets/img/red.png";
import secondItem from "@/assets/img/white.png";

const products = [
  { image: item, price: '21 999₽', label: "HOT" },
  { image: secondItem, price: '21 999₽', label: "PRE-LOVER" },
  { image: item, price: '21 999₽', label: "-40%" },
  { image: secondItem, price: '21 999₽' , label: "HOT"},
];

const isMobile = computed(() => window.innerWidth <= 768);
</script>

<template>
  <div class="popular">
    <div class="popular__header">
      <h1>Самое популярное сейчас</h1>
      <button class="popular__header__btn">Перейти</button>
    </div>

    <div class="popular__items">
      <CardComponent
          v-for="(product, index) in products"
          :key="index"
          :product="product"
          :isMobile="isMobile"
      />
    </div>
  </div>
</template>

<style scoped>
.popular {
  margin-top: 115px;
  position: relative;
}

.popular__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.popular__header h1 {
  font-size: 40px;
  font-family: "Ruberoid-Regular", sans-serif;
  font-weight: 400;
}

.popular__header__btn {
  width: 96px;
  height: 36px;
  border: 1px solid #B3B3B3;
  border-radius: 15px;
  background: none;
  font-size: 13px;
  font-family: "Inter", sans-serif;
  font-weight: 400;
}

.popular__items {
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
  gap: 20px;
}

@media (max-width: 768px) {
  .popular__items {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .popular {
    padding: 10px 10px;
    margin: 0;
    margin-top: 72px;
  }

  .popular__header h1 {
    font-size: 27px;
  }

  .popular__header__btn {
    display: none;
  }
}
</style>
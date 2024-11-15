<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  },
  isMobile: {
    type: Boolean,
    required: true
  },
  label: {
    type: String,
  }
});
</script>

<template>
  <div class="popular__item">
    <div class="popular__item__header">
      <span :class="{'hot-mobile': isMobile}">{{product.label}}</span>
      <img src="@/assets/img/favorite.png" alt="">
    </div>
    <img :src="product.image" alt="product image" class="popular__item__image">
    <div class="popular__item__description">
      <p>Сумка <span>Jacquemus</span> <br> Le Bambidou</p>
    </div>
    <div class="popular__item__price">
      <span>{{ product.price }}</span>
    </div>
  </div>
</template>

<style scoped>
.popular__item__header span {
  background: black;
  color: #fff;
  padding: 10px 15px;
  border-radius: 15px;
  font-family: "Inter", sans-serif;
  font-size: 13px;
}
.popular__item {
  width: 100%;
  max-width: 300px;
  background: none;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  border: 1px solid #D6D6D6;
  box-sizing: border-box;
}

.popular__item__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.popular__item__header span {
  background: black;
  color: #fff;
  padding: 10px 15px;
  border-radius: 15px;
  font-family: "Inter", sans-serif;
  font-size: 13px;
}

.popular__item__image {
  width: 100%;
  height: auto;
  margin-top: 15px;
}

.popular__item__description {
  color: #3E3E3E;
  font-weight: 400;
  font-size: 15px;
  margin-bottom: 15px;
}

.popular__item__description span {
  font-weight: 800;
}

.popular__item__price span {
  font-size: 15px;
  font-weight: 400;
  color: #3E3E3E;
  font-family: "Ruberoid-Regular", sans-serif;
}


@media (max-width: 768px) {
  .popular__item__header span {
    background: #FFE6E1;
    font-size: 14px;
    color: #FF7F62;
  }
  .popular__item {
    max-width: 100%;
  }

}
</style>
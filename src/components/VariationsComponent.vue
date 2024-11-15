<script setup>
import photo from "@/assets/img/variatn.png"

const variations = [
  { img: photo, text: 'покупка' },
  { img: photo, text: 'доставка' },
  { img: photo, text: 'pre-loved' },
  { img: photo, text: 'custom' },
  { img: photo, text: 'custom' },
  { img: photo, text: 'консьерж' },
];
</script>

<template>
  <div class="variations">
    <div v-for="(variation, index) in variations" :key="index" class="variation__details">
      <img :src="variation.img" alt="" />
      <h6>{{ variation.text }}</h6>
    </div>
  </div>
</template>

<style scoped>
.variations {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  padding-top: 50px;
}
.variation__details {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.variation__details h6 {
  font-size: 15px;
  font-family: "Ruberoid-Regular", sans-serif;
  color: #000000;
  font-weight: 400;
}
.variation__details img {
  margin-bottom: 12px;
}
@media (max-width: 1189px) {
  .variation__details:nth-child(n+5) {
    display: none;
  }
}
</style>
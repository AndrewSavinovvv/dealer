<script setup>

</script>

<template>
   <div class="variations">
   <div class="variation__details">
     <img src="@/assets/img/variatn.png" alt="">
     <h6>покупка</h6>
   </div>
     <div class="variation__details">
       <img src="@/assets/img/dostavka.png" alt="">
       <h6>доставка</h6>
     </div>
     <div class="variation__details">
       <img src="@/assets/img/pre.png" alt="">
       <h6>pre-loved</h6>
     </div>
     <div class="variation__details">
       <img src="@/assets/img/custom.png" alt="">
       <h6>custom</h6>
     </div>
     <div class="variation__details">
       <img src="@/assets/img/custom2.png" alt="">
       <h6>custom</h6>
     </div>
     <div class="variation__details">
       <img src="@/assets/img/cons.png" alt="">
       <h6>консьерж</h6>
     </div>
   </div>
</template>

<style scoped>
.variations {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  margin-top: 50px;
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
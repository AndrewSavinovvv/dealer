<script setup>


const categories = [
  { title: "одежда"},
  { title: "обувь"},
  { title: "акссесуары"},
  { title: "сумки"},
]
</script>

<template>
  <div class="categories">
    <div class="categories__left">
    <div class="categories__left__clothes">
      <h4>одежда</h4>
    </div>
      <div class="categories__left__footwear" >
        <h4>обувь</h4>
      </div>
    </div>
    <div class="categories__right">
    <div class="categories__right__accessory">
      <h4>аксессуары</h4>
    </div>
      <div class="categories__right__bag">
        <h4>сумки</h4>
      </div>
      <div class="categories__right__sport">
        <h4>для спорта</h4>
      </div>
    </div>
    <div v-for="(cat, index) in categories" :key="index" class="categories__mobile">
      <h4>{{ cat.title }}</h4>
    </div>
  </div>
</template>

<style scoped>
.categories {
  margin-top: 89px;
  display: flex;
  gap: 22px;
  justify-content: space-between;
}
.categories__left {
  display: flex;
  gap: 22px;
  width: 65%;
}
.categories__left__clothes {
  background-image: url("@/assets/img/photo.png");
  width: 100%;
  height: 470px;
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 40px;
  display: flex;
  align-items: flex-end;
}
.categories__left__footwear{
  background-image: url("@/assets/img/photo2.png");
  width: 100%;
  height: 470px;
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 40px;
  display: flex;
  align-items: flex-end;
}
.categories__left__clothes h4,.categories__left__footwear h4 {
  display: flex;
  padding-left: 30px;
}
.categories__right__accessory {
  background-image: url("@/assets/img/photo3.png");
 width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  display: flex;
  align-items: flex-end;
}
.categories__right__bag {
  background-image: url("@/assets/img/photo4.png");
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  display: flex;
  align-items: flex-end;
}
.categories__right__sport {
  background-image: url("@/assets/img/photo5.png");
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  display: flex;
  align-items: flex-end;
}
.categories__mobile {
  display: none;
}
.categories__right {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: white;
  font-size: 40px;
  font-family: "Inter", sans-serif;
  font-weight: 500;
  width: 32%;
}
.categories__right__accessory h4 ,.categories__right__bag h4 , .categories__right__sport h4 {
  padding-left: 23px;
  padding-bottom: 20px;
}
@media (max-width: 777px) {
  .categories {
    padding-left: 10px;
    padding-right: 10px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
  .categories__left,
  .categories__right {
    display: none;
  }
  .categories__mobile {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    height: 250px;
    width: 100%;
    background-image: url("@/assets/img/Rectangle 70.png");
    background-repeat: no-repeat;
    border-radius: 5%;
  }
  .categories__mobile h4 {
    color: white;
    display: flex;
    align-items: end;
    padding: 15px 7px;
  }
}
</style>
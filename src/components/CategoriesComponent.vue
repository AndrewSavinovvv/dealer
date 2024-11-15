<script setup>

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
  </div>
</template>

<style scoped>
.categories {
  margin-top: 89px;
  padding-left: 120px;
  margin-right: 120px;
  display: flex;
  gap: 22px;
  justify-content: space-between;
}
.categories__left {
  display: flex;
  gap: 22px;
}
.categories__left__clothes {
  background-image: url("@/assets/img/photo.png");
  width: 383px;
  height: 470px;
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 40px;
  display: flex;
  align-items: flex-end;
}
.categories__left__footwear{
  background-image: url("@/assets/img/photo2.png");
  width: 383px;
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
  height: 142px;
  width: 383px;
  display: flex;
  align-items: flex-end;
}
.categories__right__bag {
  background-image: url("@/assets/img/photo4.png");
  height: 142px;
  width: 383px;
  display: flex;
  align-items: flex-end;
}
.categories__right__sport {
  background-image: url("@/assets/img/photo5.png");
  height: 142px;
  width: 383px;
  display: flex;
  align-items: flex-end;
}
.categories__right {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-end;
  color: white;
  font-size: 40px;
  font-family: "Inter", sans-serif;
  font-weight: 500;
}
.categories__right__accessory h4 ,.categories__right__bag h4 , .categories__right__sport h4 {
  padding-left: 23px;
  padding-bottom: 20px;
}
@media (max-width: 1340px) {
  .categories {
    padding-left: 10px;
    padding-right: 10px;
    margin-right: 0;;
  }
  .categories__left,
  .categories__right {
    flex-direction: column;
    gap: 10px;
  }
  .categories__left__clothes,
  .categories__left__footwear,
  .categories__right__accessory,
  .categories__right__bag {
    width: 200px;
    height: 240px;
  }
  .categories__right__sport {
    display: none;
  }
  .categories__right__bag {
    background-image: url("@/assets/img/Rectangle 72.png");
  }
  .categories__right__accessory {
    background-image: url("@/assets/img/Rectangle 70.png");

  }
  .categories__left__clothes h4,.categories__left__footwear h4,.categories__right__accessory h4 ,.categories__right__bag h4 , .categories__right__sport h4 {
    font-size: 20px;
    padding: 7px 15px;
    font-weight: 500;
  }
}
</style>
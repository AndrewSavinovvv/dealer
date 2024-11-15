<script setup>
</script>

<template>
  <div class="main">
    <div class="header">
      <div class="burger__menu">
        <div></div>
        <div></div>
        <div></div>
      </div>
      <nav class="navigation">
        <a href="#">Одежда</a>
        <a href="#">Обувь</a>
        <a href="#">Аксессуары</a>
        <a href="#">Сумки</a>
        <a href="#">Товары для спорта</a>
      </nav>
      <div class="logo">
        <img src="@/assets/img/logo.png">
      </div>
      <div class="icons">
        <i class="icon">
          <img src="@/assets/icons/favorit.svg" alt="">
        </i>
        <i class="icon">
          <img src="@/assets/icons/basket.svg" alt="">
        </i>
        <i class="icon">
          <img src="@/assets/icons/search.svg" alt="">
        </i>
      </div>
    </div>

    <div class="main__content">
      <div class="main__content__text">
        <h1 class="main__content__title">распродажа <br>
          товаров для неё</h1>
        <p class="main__content__sale">скидки до 90%!</p>
      </div>
      <button class="main__content__btn">Перейти в каталог</button>
    </div>
    <div class="main__slider">
      <div class="slider__bar"></div>
      <div class="slider__bar"></div>
      <div class="slider__bar"></div>
      <div class="slider__bar"></div>
      <div class="slider__bar"></div>
    </div>
  </div>
</template>

<style scoped>
.main {
  background-image: url("@/assets/img/background.png");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  height: 750px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 28px;
  padding-right: 128px;
  padding-left: 128px;
}

.navigation {
  display: flex;
  gap: 15px;
}

.navigation a {
  text-decoration: none;
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 14px;
  font-weight: 400;
}

.icons {
  display: flex;
  gap: 15px;
}

.logo {
  padding-right: 300px;
}

.icon {
  font-size: 26px;
  cursor: pointer;
}

.main__content {
  margin-top: 110px;
  padding-left: 120px;
  position: relative;
}

.main__content__title {
  font-size: 66px;
  font-weight: 400;
  text-transform: uppercase;
  color: white;
}

.main__content__sale {
  position: absolute;
  top: 36px;
  left: 600px;
  background: black;
  color: white;
  padding: 12px 22px;
  text-align: center;
  font-family: "Inter", sans-serif;
  font-size: 14px;
  border-radius: 15px;
  transform: rotate(5deg);
}

.main__content__btn {
  border: 1px solid #B3B3B3;
  background: linear-gradient(#F9F8F7, #FFFFFF);
  color: #5E5E5E;
  font-size: 13px;
  font-family: "Inter", sans-serif;
  font-weight: 400;
  padding: 20px 40px;
  border-radius: 15px;
  cursor: pointer;
  margin-top: 21px;
}

.main__slider {
  display: flex;
  justify-content: center;
  gap: 8px;
  margin-top: 325px;
}

.slider__bar {
  width: 72px;
  height: 2px;
  background:#FFFFFF5E;
  border-radius: 4px;
  position: relative;
}

.slider__bar:first-child {
  background: #FFFFFF5E;
}

.slider__bar:first-child::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 50%;
  height: 100%;
  background: linear-gradient(#FFFFFF ,#999999 );
  border-radius: 4px;
}
.burger__menu {
  display: none;
}


@media (max-width: 1189px) {
  .navigation {
    display: none;
  }
  .logo {
    padding-right: 0;
  }
  .icons {
    gap: 10px;
  }
  .burger__menu {
    display: block;
    cursor: pointer;
  }
  .burger__menu div {
    width: 30px;
    height: 1px;
    background-color: white;
    margin: 6px 0;
  }
  .icon:nth-child(1) {
    display: none;
  }
  .header {
    display: flex;
   justify-content: space-between;
    align-items: center;
    padding: 20px;
  }
  .main__content {
    padding: 0 20px;

  }
  .main__content__sale {
    position: relative;
    top: -2px;
    left: 0;
    width: 110px;
  }
  .main__content__title {
    font-size: 30px;
  }
  .main {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-position: 80% center;
  }
  .main__slider {
    margin: 0;
    padding-bottom: 30px;
  }
}
</style>
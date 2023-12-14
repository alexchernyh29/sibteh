<script setup>
import { RouterLink, RouterView } from 'vue-router'
import ButtonUi from './components/ui/ButtonUi.vue'
</script>

<template>
  <header>
    <div class="wrap">
      <img alt="logo" class="logo" src="@/assets/images/logo.png"/>
      <h4>Авторизация</h4>
      <input type="text" placeholder="Логин">
      <input type="text" placeholder="Пароль">
      <ButtonUi>Вход</ButtonUi>
      <ButtonUi cssClass="white">Вход</ButtonUi>
      <ButtonUi cssClass="white-border">Вход</ButtonUi>
    </div>
    <div class="wrapper">
      
      <div class="wrapper__item">
        <p class="wrapper__item-text">Если возникла проблема, то можете написать <RouterLink to="/about">Алёне из Сибтеха</RouterLink></p>
        <p class="wrapper__item-text">С любовью, ваш <RouterLink to="/about">Сибтех</RouterLink></p>
      </div>
    </div>
  </header>
  <RouterView />
  <img alt="cube" class="main-img" src="@/assets/images/main-cube.png"/>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  background-color: #fff;
  border-radius: 10px;
  padding: 80px 95px 60px 165px;
}
.wrap {
  display: flex;
  flex-direction: column;
}
.main-img {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 800px;
  height: 650px;
}
.main-img img {
  width: 100%;
  height: 100%;
}
input {
  border-radius: 10px;
  background: #F6F6F6;
  color: #000;
  border: none;
  height: 70px;
  width: 350px;
  padding-left: 30px;
  margin-top: 10px;
  margin-bottom: 30px;
}
input::placeholder {
  opacity: 0.5;
}
input:nth-child(2) {
  margin-top: 0px;
  margin-bottom: 0px;
}
h4 {
  color: #000;
  font-family: Cera Pro;
  font-size: 40px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  margin-top: 30px;
  margin-bottom: 30px;
}
.logo {
  width: 117px;
  height: 30px;
  flex-shrink: 0;
}

.wrapper__item-text {
  color: #676767;
  font-family: Cera Pro;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: -0.64px;
  max-width: 260px;
  margin-top: 8px;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  header .wrapper {
    display: flex;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>

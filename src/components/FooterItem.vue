<script setup>
     import { RouterLink } from 'vue-router';
</script>

<template>
     <footer class="footer background_white">
          <div class="footer__left">
               <p class="footer__title">Ссылки</p>
               <div class="footer__links">
                    <RouterLink to="/" class="footer__link background_orange">Главная</RouterLink>
                    <RouterLink to="/newsList" class="footer__link background_orange">Новости</RouterLink>
                    <RouterLink to="/gameList" class="footer__link background_orange">Игры</RouterLink>
                    <RouterLink to="/signIn" class="footer__link background_orange">Вход</RouterLink>
                    <RouterLink to="/register" class="footer__link background_orange">Регистрация</RouterLink>
               </div>
          </div>
          <div class="footer__right">
               <p class="footer__title">Соц. Сети</p>
               <a href="https://github.com/SergeiKachilov/GameNews" target="_blank" class="footer__github"><img src="../components/icons/github.svg" alt=""></a>
          </div>
     </footer>
</template>

<style>
     .footer {
          display: flex;
          flex-direction: row;
          justify-content: center;
          align-items: center;
          padding: 1rem;
          gap: 5rem;
          flex-wrap: wrap;
          font-size: 0.7rem;
          margin-top: 1rem;
          border-radius: 1rem;
     }

     .footer__left {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: center;
          gap: 1rem;
          height: 100%;
     }

     .footer__title {
          font-size: 1rem;
          margin: 0;
          font-weight: bold;
     }

     .footer__links {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
          gap: 1rem;
          font-size: 1rem;
     }

     .footer__link {
          text-decoration: none;
          color: black;
          padding: 0 1rem;
          border-radius: 41px;

     }

     .footer__right {
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: center;
          gap: 1rem;
     }
</style>
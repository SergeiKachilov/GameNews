<script setup>
     import { RouterLink } from 'vue-router'
</script>

<template>
     <header class="header background_white">
          <div class="header__title background_orange">
              <img src="./icons/logo.png" alt="" class="header__logo"> 
              <RouterLink to="/" class="header__title-a header__a">GameVox</RouterLink>
          </div>
          <nav class="header__nav background_orange">
              <RouterLink to="/newsList" class="header__nav-a header__a">Новости</RouterLink>
              <RouterLink to="/gameList" class="header__nav-a header__a">Игры</RouterLink>
              <div class="header__search header__a">
                  <RouterLink to="/" class="header__nav-a header__a"><img src="./icons/searchIcon.svg" alt="" class="header__search-icon">Поиск</RouterLink>

              </div>
          </nav>
          <div class="header__authorization background_orange">
               <RouterLink to="/signIn" class="header__authorization-btn">
                    <div class="header__a header__authorization-a">
                         <p class="header__a"><img src="./icons/authorizationIcon.svg" alt="" class="header__authorization-icon">Вход | Регистрация</p>
                    </div>
               </RouterLink>
          </div>
     </header>
</template>

<style scoped>
     .header {
          width: 100%;
          height: 4.2em;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          gap: 1.1rem;
          font-size: 2rem;
          border-radius: 15px;
          box-sizing: border-box;
          padding: 0.7rem;
          margin-bottom: 1rem;
     }

     .header__title {
          width: 10em;
          height: 5.6rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          border-radius: 41px;
          padding: 0 1.1rem;
     }

     .header__logo {
          border-radius: 50%;
          width: 4.4rem;
     }

     .header__a {
          display: flex;
          justify-content: center;
          align-items: center;
          text-align: center;
          font-weight: bold;
          color: rgba(0, 0, 0, 1);
          text-decoration: none;
          background-color: rgba(255, 131, 0, 1);
          border-radius: 41px; 
          margin: 0px;
     }

     .header__title-a {
          max-width: 12.4rem;
          width: 100%;
          height: 3.7rem;
     }

     .header__nav {
          width: 19.7em;
          height: 5.6rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          border-radius: 41px;
          padding: 0 1.1rem;
          gap: 1.1rem;
     }

     .header__nav-a {
          max-width: 12.3rem;
          width: 100%;
          height: 3.7rem;
          padding: 0 1rem;
          box-sizing: border-box;
     }

     .header__search {
          max-width: 12.3rem;
          width: 100%;
          height: 3.7rem;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
          padding: 0 auto;
     }

     .header__search-icon {
          max-width: 1.7rem;
          width: 100%;
          margin-right: 0.6rem;
     }

     .header__authorization {
          width: 14.4em;
          height: 5.6rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
          border-radius: 41px;
          padding: 0 1.1rem;
          font-size: 1.5rem;
     }
     
     .header__authorization-btn {
          width: 100%;
          display: flex;
          text-decoration: none;
     }

     .header__authorization-a {
          max-width: 22.2rem;
          width: 100%;
          height: 3.7rem;
          padding: 0 0.6rem;
     }

     .header__authorization-icon {
          max-width: 1.7rem;
          width: 100%;
          margin-right: 0.6rem;
     }

     @media (max-width: 565px) {
          .header {
               display: flex;
               flex-direction: column;
               height: auto;
               width: auto;
               padding: 1rem;
          }

          .header__nav {
               flex-direction: column;
               height: auto;
               width: auto;
               padding: 1rem;
               border-radius: 15px;
               width: 10em;
          }

          .header__nav-a, .header__search {
               width: 100%;
               max-width: none;
          }
     }
</style>

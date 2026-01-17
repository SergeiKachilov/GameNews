<script setup>
     import { RouterLink } from 'vue-router';
     
</script>

<template>
     <div class="main-body">
          <div class="signin background_white">
               <p class="signin__title background_orange">Вход</p>
               <input type="text" class="signin__login background_orange" placeholder="Логин">
               <input type="password" class="signin__password background_orange" placeholder="Пароль">
               <div class="signin__btn-container background_orange">
                    <button class="signin__btn background_orange">Войти</button>
               </div>
               <p class="signin__register">Нет аккаунта? <RouterLink to="/register" class="signin__register-btn background_orange">Зарегистрироваться</RouterLink></p>
          </div>
     </div>
</template>

<style scoped>
     .main-body {
          width: 100%;
          display: flex;
          flex-direction: column;
          align-items: center;
     }

     .signin {
          width: 40%;
          padding: 1rem;
          border-radius: 15px;
          font-size: 2rem;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          gap: 1.5rem;
          align-items: center;
     }

     .signin__title {
          width: 40%;
          padding: 0 1rem;
          border-radius: 41px;
          text-align: center;
          font-weight: bold;
          font-size: 2.5rem;
          margin: 0;
          box-sizing: border-box;
     }

     .signin__login, .signin__password {
          font-size: 2rem;
          text-align: center;
          border-radius: 41px;
     }

     .signin__btn-container {
          width: 40%;
          padding: 1rem;
          font-size: 2rem;
          border-radius: 41px;
          font-weight: bold;
          box-sizing: border-box;
     }

     .signin__btn {
          background-color: rgba(255, 131, 0, 1);
          font-size: 2rem;
          width: 100%;
          height: 100%;
          box-sizing: border-box;
          padding: 0.5rem 1rem;
          border-radius: 41px;
          border: none;
          font-weight: bold;
     }

     .signin__register {
          font-size: 1.5rem;
     }

     .signin__register-btn {
          padding: 0 1rem;
          border-radius: 41px;
          text-decoration: none;
          color: black;
          font-weight: bold;
     }
</style>
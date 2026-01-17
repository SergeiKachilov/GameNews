<script setup>
     import { RouterLink } from 'vue-router';
     import { ref, watch } from 'vue';

     const login = ref("");
     const email = ref("");
     const password = ref("");
     const confirm = ref("");
     const alert_message = ref("");

     function CheckPassword() {
          if (password.value == confirm.value) {
               return true;
          }
          alert_message.value = "Пароли не совпадают!"
          return false;
     }

     function CheckEmail() {
          let pattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
          return pattern.test(email.value);
     }

     function CheckData() {
          if(CheckEmail()) {
               if(CheckPassword()) {
                    alert("Успешная регистрация");
               }
          }
          else {
               alert_message.value = "Неверный формат почты!"
          }
     }

     watch([login, email, password, confirm], () => {
          alert_message.value = "";
     })
</script>

<template>
     <div class="main-body">
          <div class="register background_white">
               <p class="register__title background_orange">Регистрация</p>
               <input type="text" class="register__input background_orange" placeholder="Логин" required v-model="login">
               <input type="email" class="register__input background_orange" placeholder="Почта" required v-model="email">
               <input type="password" class="register__input background_orange" placeholder="Пароль" required v-model="password">
               <input type="password" class="register__input background_orange" placeholder="Повторите пароль" required v-model="confirm">
               <div class="register__btn-container background_orange">
                    <button class="register__btn background_orange" type="submit" @click="CheckData()">Зарегистрироваться</button>
               </div>
               <p class="register__alert" v-if="alert_message != ''">{{ alert_message }}</p>
               <p class="register__signin">Уже есть аккаунт? <RouterLink to="/signin" class="register__signin-btn background_orange">Войти</RouterLink></p>
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

     .register {
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

     .register__title {
          /* width: 40%; */
          padding: 0 2rem;
          border-radius: 41px;
          text-align: center;
          font-weight: bold;
          font-size: 2.5rem;
          margin: 0;
          box-sizing: border-box;
     }

     .register__input {
          font-size: 2rem;
          text-align: center;
          border-radius: 41px;
     }

     .register__btn-container {
          /* width: 40%; */
          padding: 1rem;
          font-size: 2rem;
          border-radius: 41px;
          font-weight: bold;
          box-sizing: border-box;
     }

     .register__btn {
          cursor: pointer;
     }

     .register__btn {
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

     .register__signin {
          font-size: 1.5rem;
     }

     .register__signin-btn {
          padding: 0 1rem;
          border-radius: 41px;
          text-decoration: none;
          color: black;
          font-weight: bold;
     }

     .register__alert {
          margin: 0;
          color: red;
     }
</style>
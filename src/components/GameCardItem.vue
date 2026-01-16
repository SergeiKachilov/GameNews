<script setup>
     import { defineProps } from 'vue';

     const props = defineProps ({
          id: {
               type: Int32Array,
          },
          name: {
               type: String,
          },
          genre: {
               type: Array,
          },
          logo: {
               type: String,
          },
          developer: {
               type: String,
          },
          steam_rating: {
               type: Float32Array,
          },
          site_rating: {
               type: Float32Array,
          },
          release_date: {
               type: String,
          },
          text: {
               type: String,
          },
          comments: {
               type: Array,
          }
     })
</script>

<template>
     <RouterLink :to="{name: 'game', params: {gameId: id}}" class="game background_white">
          <img :src="logo" alt="" class="game__logo">
          <div class="game__info">
               <p class="game__name background_orange">{{name}}</p>
               <p class="game__rating background_orange">Рейтинг: {{site_rating}}</p>
          </div>
     </RouterLink>
</template>

<style scoped>
     .game {
          width: 24rem;
          height: 10rem;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          padding: 1rem;
          border-radius: 15px;
          gap: 1rem;
          text-decoration: none;
     }

     .game__logo {
          width: 7.9rem;
          height: 9.2rem;
          border-radius: 25px;
     }

     .game__info {
          width: 60%;
          font-size: 1.5rem;
          font-weight: bold;
          display: flex;
          flex-direction: column;
          justify-content: center;
          gap: 1.5rem;
     }

     .game__info p {
          margin: 0;
          border-radius: 41px;
          text-align: center;
          padding: 0 1rem;
          color: black;
          text-decoration: none;
     }
</style>
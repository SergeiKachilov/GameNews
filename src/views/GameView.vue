<script setup>
     import Comment from '@/components/Comment.vue';
     import { useRoute } from 'vue-router';
     import { onMounted, ref } from 'vue';

     const game = ref({});
     const games_json = ref([]);
     const text_array = ref([]);
     const route = useRoute();
     // let id = route.params.newsId;
     Start();

     async function Start() {
          // await fetch("/src/components/json/games.json")
          // .then((resp) => resp.json())
          // .then((json) => {
          //      games_json.value = json;
          //      console.log(json);
          // })
          await ReadJson();
          ReadTxt();
     }

     function GetInfo(id) {
          console.log("el");
          games_json.value.forEach(el => {
               if (el.id == id) {
                    console.log("asd");
                    game.value = el;
               }
          });
     }

     async function ReadJson(id) {
          await fetch("/src/components/json/games.json")
          .then((resp) => resp.json())
          .then((json) => {
               games_json.value = json;
               console.log(json);
               json.forEach(el => {
                    if (el.id == id) {
                         console.log("asd");
                         game.value = el;
                    }
               });
               GetInfo(route.params.gameId);
          })
     }

     function ReadTxt() {
          let file = game.value.text;
          fetch(file)
          .then(response => response.text())
          .then(text => {
               text_array.value = text.split('\n');
          });
     }

     onMounted(async () => {
          ReadTxt();
     })
</script>

<template>
     <div class="main-body">
          <div class="game background_white">
               <div class="game__info-container">
                    <img :src="game.logo" alt="" class="game__logo">
                    <div class="game__info">
                         <p class="game__name background_orange">{{game.name}}</p>
                         <div class="game__middle">
                              <p class="game__genres background_orange">{{ game.genre.join(', ') }}</p>
                              <p class="game__developer background_orange">{{ game.developer }}</p>
                         </div>
                         <div class="game__bottom">
                              <div class="game__rating">
                                   <p class="game__total-rating background_orange">Рейтинг Steam: {{ game.steam_rating }}</p>
                                   <p class="game__local-rating background_orange">Рейтинг на сайте: {{game.site_rating}}</p>
                              </div>
                              <p class="game__release-date background_orange">Релиз: {{game.release_date}}</p>

                         </div>
                    </div>
               </div>
               <div class="game__text background_orange">
                    <p class="game__paragraph" v-for="paragraph in text_array">{{ paragraph }}</p>
               </div>
          </div>

          <div class="comments">
               <comment v-for="comment in game.comments"
               :comment="comment"
               ></comment>
          </div>
     </div>
</template>

<style scoped>
     .main-body {
          display: flex;
          flex-direction: column;
          gap: 1rem;
     }
     .game {
          /* width: 80%; */
          padding: 1rem;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          align-items: center;
          gap: 1.5rem;
          border-radius: 15px;
     }

     .game__info p {
          margin: 0;
          box-sizing: border-box;
          display: flex;
          align-items: center;
          justify-content: center;
     }

     .game__info-container {
          width: 46.6rem;
          display: flex;
          flex-direction: row;
          justify-content: center;
          box-sizing: border-box;
          gap: 1rem;
          font-size: 1.3rem;
          text-align: center;
     }

     .game__info-container p {
          padding: 0.5rem 1rem;
          border-radius: 41px;
     }

     .game__logo {
          width: 9.2rem;
          border-radius: 25px;
     }

     .game__info {
          width: 100%;
          display: flex;
          flex-direction: column;
          gap: 1rem;
     }

     .game__name {
          font-size: 1.5rem;
          font-weight: bold;
          box-sizing: border-box;
     }

     .game__middle {
          width: 100%;
          display: flex;
          justify-content: space-between;
          gap: 1rem;
     }

     .game__genres {
          width: 80%;
     }

     .game__developer {
          width: 20%;
     }

     .game__bottom {
          width: 100%;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          gap: 1rem
     }

     .game__release-date {
          width: 20%;
          font-size: 1rem;
     }

     .game__rating {
          display: flex;
          width: 80%;
          justify-content: space-between;
          box-sizing: border-box;
          gap: 1rem;
     }

     .game__text {
          width: 55.5rem;
          font-size: 2rem;
          padding: 1.5rem 1.5rem;
          box-sizing: border-box;
          text-align: justify;
          border-radius: 15px;
     }

     .game__paragraph {
          margin: 0;
          margin-bottom: 1rem;
          text-indent: 2rem;
     }

     .comments {
          width: 100%;

          display: flex;
          flex-direction: column;
          align-items: center;     
          
          gap: 1rem;
     }
</style>
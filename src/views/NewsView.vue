<script setup>
     import Comment from '@/components/Comment.vue';
     import { onMounted, ref } from 'vue';
     import { useRoute } from 'vue-router';

     const news = ref({});
     const news_json = ref([]);
     const text_array = ref([]);
     const route = useRoute();
     // let id = route.params.newsId;

     function GetInfo(id) {
          console.log("el");
          news_json.value.forEach(el => {
               if (el.id == id) {
                    console.log("asd");
                    news.value = el;
               }
          });
     }

     function ReadTxt() {
          let file = news.value.file;
          fetch(file)
          .then(response => response.text())
          .then(text => {
               text_array.value = text.split('\n');
          });
     }

     onMounted(async () => {
          await fetch("/src/components/json/news.json")
          .then((resp) => resp.json())
          .then((json) => {
               news_json.value = json;
               console.log(json);
          })
          GetInfo(route.params.newsId);
          ReadTxt();
     })
</script>

<template>
     <div class="main-body">
          <div class="main background_white">
               <div class="main__title-container">
                    <!-- <img src="/src/components/img/RE wishlist.png" alt="" class="main__cover"> -->
                    <p class="main__title background_orange">{{ news.text }}</p>
               </div>
     
               <div class="main__info">
                    <p class="main__rating background_orange">Рейтинг {{news.rating}}</p>
                    <p class="main__type background_orange">{{ news.type }}</p>
                    <p class="main__comments background_orange"><img src="../components/icons/commentIcon.svg" alt="" class="main__comments-img">{{news.comments}}</p>
               </div>
     
               <div class="main__text-container background_orange">
                    <p class="main__text" v-for="paragraph in text_array">{{ paragraph }}</p>
               </div>
          </div>
     
          <div class="comments">
               <comment></comment>
          </div>
     </div>
</template>

<style scoped>
     .main-body {
          display: flex;
          flex-direction: column;
          gap: 1rem;
     }

     .main {
          width: 100%;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          margin-top: 1.1rem;
          border-radius: 15px;
          padding: 1rem;
          gap: 1rem;
     }
     
     .main__title-container {
          width: 78.5%;
          height: 200px;
          background-image: url("/src/components/img/RE wishlist.png");
          background-size: cover;
          background-position: center center;
          display: flex;
          justify-content: center;
          align-items: end;
          border-radius: 25px;
     }

     .main p {
          margin: 0;
     }

     .main__title {
          width: 100%;
          text-align: center;
          font-size: 2rem;
          font-weight: bold;
          border-radius: 41px;
          margin: 0;
     }

     .main__info {
          margin-top: 12px;
          margin-bottom: 12px;
          width: 34%;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
     }

     .main__rating, .main__type, .main__comments {
          font-weight: bold;
          width: 26.5%;
          display: flex;
          align-items: center;
          justify-content: center;
          border-radius: 41px;
     }

     .main__comments-img {
          height: 78.6%;
          margin-right: 10%;
     }

     .main__text-container {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          gap: 1rem;
          padding: 1rem;
          box-sizing: border-box;
          width: 94.4%;
          border-radius: 41px;

          text-align: justify;
     }

     .main__text {
          width: 82.4%;
          font-size: 1.6rem;
     }

     .comments {
          width: 100%;

          display: flex;
          flex-direction: column;
          align-items: center;
          
     }
</style>
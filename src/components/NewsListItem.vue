<script setup>
     import { defineProps } from 'vue';
     import { RouterLink } from 'vue-router';
     const props = defineProps({
          id: {
               type: String,
          },

          type: {
               type: String,
               default: "Новость",
          },

          text: {
               type: String,
               default: "...",
          },

          rating: {
               type: String,
               default: "0.0",
          },

          comments: {
               type: String,
               default: "0",
          },

          image: {
               type: String,
               default: "/"
          },

          file: {
               type: String,
               default: "/"
          }
     })
</script>

<template>
     <RouterLink :to="{name: 'news', params: {newsId: +id}}" class="main-body__news background_white">
          <img :src="image" alt="" class="main-body__news-img">
          <div class="main-body__news-info">
               <p class="main-body__news-type background_orange">{{type}}</p>
               <p class="main-body__news-content background_orange">{{text}}</p>
               <div class="main-body__news-rating-container">
                    <p class="main-body__news-rating background_orange">{{rating}}</p>
                    <div class="main-body__news-comments-container background_orange">
                            
                         <p class="main-body__news-comments"><img src="../components/icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">{{comments}}</p>
                    </div>
               </div>
          </div>
     </RouterLink>
</template>

<style scoped>
     .main-body__news {
          max-width: 100%;
          width: 100%;
          height: auto;
          display: flex;
          flex-direction: row;
          justify-content: space-around;
          align-items: center;
          padding: 0.7rem;
          text-decoration: none;
          color: black;
          font-family: "Rounded Mplus 1c Bold";
          font-weight: bold;
          border-radius: 15px;
          box-sizing: border-box;
          gap: 0.7rem;
     }

     .main-body__news-img {
          margin: 0;
          padding: 0;
          width: 14.9rem;
          box-sizing: border-box;
     }

     .main-body__news-info {
          max-width: 70.1%;
          width: 100%;
          height: 7rem;
          display: flex;
          flex-direction: column;
          align-items: baseline;
          justify-content: center;
          gap: 0.9rem;
     }

     .main-body__news-type {
          max-width: 7.3rem;
          width: 100%;
          height: 1.4rem;
          border-radius: 15px;
          margin: 0;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
     }

     .main-body__news-content {
          width: 100%;
          text-align: left;
          text-decoration: none;
          font-size: 1rem;
          border-radius: 15px;
          margin: 0;
          padding: 0.3rem 0.6rem;
          box-sizing: border-box;
     }

     .main-body__news-rating-container {
          width: 100%;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          margin: 0px;
          box-sizing: border-box;
     }

     .main-body__news-rating {
          max-width: 7.3rem;
          width: 100%;
          height: 1.4rem;
          border-radius: 15px;
          margin: 0px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
     }

     .main-body__news-comments-container {
          max-width: 7.3rem;
          width: 100%;
          height: 1.4rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          margin: 0px;
          border-radius: 15px;
          gap: 0.6rem;
     }

     .main-body__news-comments {
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
     }

     .main-body__news-comments-icon {
          max-width: 1.2rem;
          width: 100%;
          margin-right: 0.6rem;
     }
</style>
<script setup>
     import { defineProps } from 'vue';

     let props = defineProps ({
          comment: {
               type: Object,
          }
     })
</script>

<template>
     <div class="comment background_white">
          <div class="comment__top">
               <p class="comment__time background_orange">{{comment.date}}</p>
               <p class="comment__nickname background_orange">{{comment.username}}</p>
          </div>
          
          <div class="comment__middle">
               <img :src="comment.avatar" alt="" class="comment__avatar">
               <p class="comment__text background_orange">{{comment.text}}</p>
          </div>
          
          <div class="comment__bottom">
               <p class="comment__btn background_orange">-</p>
               <p class="comment__rate background_orange">{{comment.rating}}</p>
               <p class="comment__btn background_orange">+</p>
          </div>
     </div>
</template>

<style scoped>
     .comment {
          font-size: 1rem;

          display: flex;
          flex-direction: column;
          width: 44.4rem;
          box-sizing: border-box;

          padding: 1rem;
          border-radius: 15px;
          justify-content: space-between;

          gap: 0.7rem;
     }

     .comment p {
          margin: 0;
          padding: 0.5em;
          border-radius: 41px;
     }

     .comment__top {
          width: 100%;
          display: flex;
          flex-direction: row;
          justify-content: left;
          gap: 1rem;
     }

     .comment__time {
          width: 15%;
          text-align: center;
          box-sizing: border-box;
     }

     .comment__nickname {
          width: 13.6rem;
          text-align: center;
          font-weight: bold;
     }

     .comment__middle {
          width: 100%;
          justify-content: space-between;
          display: flex;
          gap: 1rem;
          align-items: center;
     }

     .comment__avatar {
          width: 19%;
          border-radius: 50%;
          box-sizing: border-box;
     }

     .comment__text {
          width: 100%;
          font-size: 1.8rem;
          padding: 1rem;
     }

     .comment__bottom {
          display: flex;
          flex-direction: row;
          justify-content: right;
          gap: 1rem;
     }

     .comment__btn {
          width: 2rem;
          height: 2rem;
          box-sizing: border-box;
          display: flex;
          justify-content: center;
          align-items: center;

          border-radius: 50%;
     }

     .comment__rate {
          box-sizing: border-box;
          max-height: 2rem;
          min-width: 2rem;
          display: flex;
          justify-content: center;
          align-items: center;
     }
</style>
<script setup>

</script>

<template>
     <div class="comment background_white">
          <div class="comment__top">
               <p class="comment__time background_orange">Сегодня, 15:18</p>
               <p class="comment__nickname background_orange">Requiem_For_A_Dream</p>
          </div>
          
          <div class="comment__middle">
               <img src="/src/components/img/Requiem.png" alt="" class="comment__avatar">
               <p class="comment__text background_orange">Пусть предзаказы открывают.</p>
          </div>
          
          <div class="comment__bottom">
               <p class="comment__btn background_orange">+</p>
               <p class="comment__rate background_orange">-1</p>
               <p class="comment__btn background_orange">-</p>
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
     }

     .comment__nickname {
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
          width: 15%;
     }

     .comment__text {
          width: 100%;
          height: 1em;
          font-size: 1.8rem;
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
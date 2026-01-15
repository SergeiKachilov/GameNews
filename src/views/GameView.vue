<script setup>
     import Comment from '@/components/Comment.vue';
</script>

<template>
     <div class="main-body">
          <div class="game background_white">
               <div class="game__info-container">
                    <img src="../components/img/RE_RequiemLogo.png" alt="" class="game__logo">
                    <div class="game__info">
                         <p class="game__name background_orange">Resident Evil Requiem</p>
                         <div class="game__middle">
                              <p class="game__genres background_orange">Экшен Приключение Хоррор Выживание</p>
                              <p class="game__developer background_orange">Capcom</p>
                         </div>
                         <div class="game__bottom">
                              <div class="game__rating">
                                   <p class="game__total-rating background_orange">Общий рейтинг: 5.0</p>
                                   <p class="game__local-rating background_orange">Рейтинг на сайте: 4.3</p>
                              </div>
                              <p class="game__release-date background_orange">27.02.2026</p>

                         </div>
                    </div>
               </div>
               <p class="game__text background_orange">Сюжет игры описывает 
                    заброшенный отель, где было обнаружено тело жертвы с 
                    неопознанной болезнью. На расследование этого дела 
                    назначается аналитик ФБР Грейс Эшкрофт. Отель имеет 
                    для неё особое значение: именно здесь восемь лет назад 
                    погибла её мать. Это обстоятельство вынуждает Грейс 
                    столкнуться с личным прошлым, а само расследование приводит 
                    к раскрытию скрытой правды о вспышке биологической катастрофы 
                    в Раккун-Сити.</p>
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

     .game p {
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
          font-size: 1.3rem;
          padding: 1.5rem 1.5rem;
          box-sizing: border-box;
          text-align: justify;
          border-radius: 15px;
     }

     .comments {
          width: 100%;

          display: flex;
          flex-direction: column;
          align-items: center;
          
     }
</style>
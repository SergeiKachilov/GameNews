<script setup>
     import Slider from '@vueform/slider';
     import { ref, onMounted } from 'vue';
     import GameCardItem from '@/components/GameCardItem.vue';

     let minYear = 1995;
     let maxYear = 2030;
     const years = ref([minYear, maxYear]);

     let minRate = 1;
     let maxRate = 5;
     const rates = ref([minRate, maxRate]);

     const game_json = ref([]);

     let step = 5;

     function SliderFormat(val) {
          if (val == minYear) {
               return "Раньше";
          }
          else if (val == maxYear) {
               return "Позже";
          }
          else {
               return val;
          }
     }

     onMounted(async () => {
          await fetch("/src/components/json/games.json")
          .then((resp) => resp.json())
          .then((json) => {
               game_json.value = json;
               console.log(json);
          })
     })
</script>

<template>
     <div class="main-body">
          <div class="filters background_white">
               <div class="filters__top">
                    <p class="filters__year background_orange">Год выхода</p>
                    <p class="filters__rating background_orange">Оценка</p>
                    <input type="text" class="filters__search background_orange" placeholder="Поиск">
               </div>
     
               <div class="filters__bottom">
                    <Slider
                      v-model="years"
                      :tooltipPosition="'bottom'"
                      :min="minYear"
                      :max="maxYear"
                      :step="step"
                      :format="SliderFormat"
                      class="filters__slider"
                    ></Slider>
     
                    <Slider
                      v-model="rates"
                      :tooltipPosition="'bottom'"
                      :min="minRate"
                      :max="maxRate"
                      class="filters__slider"
                    ></Slider>
     
                    <select name="" id="" class="filters__sort background_orange">
                         <option value="" class="filters__sort-option">Сортировка...</option>
                         <option value="" class="filters__sort-option">По названию</option>
                         <option value="" class="filters__sort-option">По году выпуска</option>
                         <option value="" class="filters__sort-option">По рейтингу</option>
                    </select>
               </div>
          </div>

          <div class="games">
               <game-card-item v-for="game in game_json"
               :id="game.id"
               :name="game.name"
               :genre="game.genre"
               :logo="game.logo"
               :developer="game.developer"
               :steam_rating="game.steam_rating"
               :site_rating="game.site_rating"
               :release_date="game.release_date"
               :text="game.text"
               :comments="game.comments"
               ></game-card-item>
          </div>
     </div>
</template>

<!-- <script>
  import Slider from '@vueform/slider'

  export default {
    components: { Slider },
    data: () => ({
      value: [20, 40]
    })
  }
</script> -->

<style src="@vueform/slider/themes/default.css"></style>

<style scoped>
     .main-body {
          display: flex;
          flex-direction: column;
          gap: 1rem;
     }

     .filters {
          padding: 1.5rem;
          padding-bottom: 2.5rem;
          border-radius: 15px;
          
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          gap: 1rem;
     }

     .filters__top {
          width: 100%;
          display: flex;
          justify-content: space-around;
          align-items: center;
     }

     .filters__year, .filters__rating, .filters__search, .filters__sort {
          width: 16.6rem;
          margin: 0;
          font-size: 2rem;
          padding: 0.5rem;
          box-sizing: border-box;
          border-radius: 41px;
          text-align: center;
          font-weight: bold;
     }

     .filters__bottom {
          display: flex;
          flex-direction: row;
          width: 100%;
          justify-content: space-around;
          align-items: center;
     }

     .filters__sort {
          font-size: 1.5rem;
          display: flex;
          justify-content: center;
          align-items: center;
          background-position: 5rem;
     }

     .filters__slider {
          width: 16rem;
          --slider-connect-bg: black;
          --slider-handle-bg: #FF8300;
          --slider-tooltip-bg: #FFBB73;
          --slider-tooltip-color: black;
     }

     .games {
          display: flex;
          flex-direction: row;
          justify-content: center;
          flex-wrap: wrap;
          gap: 1rem;
     }
</style>
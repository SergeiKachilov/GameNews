<script setup>
    import NewsListItem from '@/components/NewsListItem.vue';
    import FooterItem from '@/components/FooterItem.vue';

    import {ref, onMounted} from 'vue';
    import { RouterLink } from 'vue-router';

    const news_json = ref([]);

    onMounted(() => {
        fetch("src/components/json/news.json",)
        .then((resp) => resp.json())
        .then((json) => {
            news_json.value = json;
            console.log(json);
        })
    })
</script>

<template>
  <div class="main-body">
        <div class="main-body__news-list">
            <news-list-item v-for="news in news_json"
                :news="news"
            ></news-list-item>
            <!-- <a href="" class="main-body__news background_white">
                <img src="../components/img/RE Requiem.png" alt="" class="main-body__news-img">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">Resident Evil Requiem добавили в вишлист более 2 млн раз</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 5.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="../components/icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">32</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="../components/img/Dying Light.png" alt="" class="main-body__news-img">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Видеообзор</p>
                    <p class="main-body__news-content background_orange">Dying Light: The Beast: Ты человек или кто</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 4.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="../components/icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">10</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="../components/img/Clair Obscur.png" alt="" class="main-body__news-img">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">У Clair Obscur: Expedition 33 больше всего номинаций на Golden Joystick Awards 2025</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 4.5</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="../components/icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">11</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="../components/img/Helldivers 2.png" alt="" class="main-body__news-img">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">Авторы Helldivers 2 пояснили, почему на ПК игра занимает так много места</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 3.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="../components/icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">22</p>
                        </div>
                    </div>
                </div>
            </a> -->
        </div>

        <div class="main-body__game-container">
            <RouterLink to="/game" class="main-body__game background_white">
                <img src="../components/img/Silent Hill f.png" alt="" class="main-body__game-icon">
                <div class="main-body__game-info">
                    <p class="main-body__game-name background_orange">Silent Hill f</p>
                    <p class="main-body__game-rating background_orange">Рейтинг 3.5</p>
                </div>
            </RouterLink>

            <div class="main-body__game-comments">
                <div class="main-body__game-comment-container background_white">
                    <img src="../components/img/AshBornd.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">AshBornd</p>
                        <p class="main-body__comment-content background_orange">Инди хоррор из steam за 200 рублей.</p>
                       <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="main-body__game-comment-container background_white">
                    <img src="../components/img/Alexander.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">Александр Матвейчук</p>
                        <p class="main-body__comment-content background_orange">Хорошая игра</p>
                       <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="main-body__game-comment-container background_white bottom-radius_15">
                    <img src="../components/img/GaryZhelezo.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">GaryZhelezo</p>
                        <p class="main-body__comment-content background_orange">Хороший хоррор, средний соулс-лайк</p>
                        <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="../components/icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
  .main-body {
        width: 100%;
        display: flex;
        /* flex-direction: row; */
        justify-content: space-between;
        gap: 0.6rem;
        margin: 0px auto;
        padding: 0px;
        flex-wrap: wrap;
        vertical-align: top;
        /* border: solid black; */
     }

     .main-body__news-list {
          /* max-width: 60%; */
          width: 100%;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          gap: 0.6rem;
          margin: 0px;
          vertical-align: top;
     }

     

     .main-body__game-container {
          width: 100%;
          height: 100%;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          gap: 0.6rem;
          margin: 0;
     }

     .main-body__game {
          max-width: 100%;
          width: 100%;
          height: 12.3rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          text-decoration: none;
          color: black;
          font-size: 2rem;
          font-weight: bold;
          text-align: center;
          border-top-left-radius: 15px;
          border-top-right-radius: 15px;
          padding-top: 0.6rem;
          padding-bottom: 0.6rem;
     }

     .main-body__game-icon {
          max-width: 9.2rem;
          width: 100%;
     }

     .main-body__game-info {
          max-width: 17.2rem;
          width: 100%;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          gap: 1.7rem;
     }

     .main-body__game-name {
          margin: 0px;
          text-decoration: underline;
          border-radius: 15px;
     }

     .main-body__game-rating {
          margin: 0px;
          border-radius: 15px;
     }

     .main-body__game-comments {
          max-width: 100%;
          width: 100%;
          height: 24.6rem;
          display: flex;
          flex-direction: column;
          justify-content: baseline;
          gap: 0.6rem;
     }

     .bottom-radius_15 {
          border-bottom-left-radius: 15px;
          border-bottom-right-radius: 15px;
     }

     .main-body__game-comment-container {
          max-width: 100%;
          width: 100%;
          height: 7.2rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          gap: 0.5rem;
          margin: 0px;
     }

     .main-body__user-avatar {
          max-width: 13.3%;
          width: 100%;
          margin: 0px;
     }

     .main-body__game-comment {
          max-width: 78.2%;
          width: 100%;
          height: 6.4rem;
          display: flex;
          flex-direction: column;
          gap: 0.5rem;
     }

     .main-body__username {
          max-width: 10.7rem;
          width: 100%;
          height: 10.5rem;
          margin: 0;

          border-radius: 15px;
          font-size: 1rem;
          font-weight: bold;
          text-align: center;
     }

     .main-body__comment-content {
          max-width: 98%;
          width: 100%;
          height: 60.3rem;
          border-radius: 15px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: baseline;
          font-size: 1.2rem;
          font-weight: bold;
          padding: auto;
          padding-left: 0.6rem;
          margin: 0px;
     }

     .main-body__user-rating-container {
          max-width: 100%;
          width: 100%;
          height: 1.3rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: end;
     }

     .main-body__user-rating {
          max-width: 6.6rem;
          width: 100%;
          height: 1.3rem;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
          border-radius: 15px;
     }

     .main-body__rate-star {
        width: 14.2%;
     }

     .unactive-star {
          opacity: 50%;
     }
</style>
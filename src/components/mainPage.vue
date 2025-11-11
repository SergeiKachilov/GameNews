<script setup>

</script>

<template>
     <header class="header background_white">
        <div class="header__title background_orange">
            <img src="./icons/logo.png" alt="" class="header__logo"> 
            <a href="" class="header__title-a header__a">GameVox</a>
        </div>
        <nav class="header__nav background_orange">
            <a href="" class="header__nav-a header__a">Новости</a>
            <a href="" class="header__nav-a header__a">Игры</a>
            <div class="header__search header__a">
                <a href="" class="header__nav-a header__a"><img src="./icons/searchIcon.svg" alt="" class="header__search-icon">Поиск</a>
                
            </div>
        </nav>
        <div class="header__authorization background_orange">
            <div class="header__a header__authorization-a">
                <a href="" class="header__a"><img src="./icons/authorizationIcon.svg" alt="" class="header__authorization-icon">Вход | Регистрация</a>
            </div>
        </div>
    </header>

    <div class="main-body">
        <div class="main-body__news-list">
            <a href="" class="main-body__news background_white">
                <img src="./img/RE Requiem.png" alt="" class="main-body__news-img">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">Resident Evil Requiem добавили в вишлист более 2 млн раз</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 5.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="./icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">32</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="./img/Dying Light.png" alt="">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Видеообзор</p>
                    <p class="main-body__news-content background_orange">Dying Light: The Beast: Ты человек или кто</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 4.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="./icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">10</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="./img/Clair Obscur.png" alt="">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">У Clair Obscur: Expedition 33 больше всего номинаций на Golden Joystick Awards 2025</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 4.5</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="./icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">11</p>
                        </div>
                    </div>
                </div>
            </a>

            <a href="" class="main-body__news background_white">
                <img src="./img/Helldivers 2.png" alt="">
                <div class="main-body__news-info">
                    <p class="main-body__news-type background_orange">Новость</p>
                    <p class="main-body__news-content background_orange">Авторы Helldivers 2 пояснили, почему на ПК игра занимает так много места</p>
                    <div class="main-body__news-rating-container">
                        <p class="main-body__news-rating background_orange">Рейтинг 3.0</p>
                        <div class="main-body__news-comments-container background_orange">
                            
                            <p class="main-body__news-comments"><img src="./icons/commentIcon.svg" alt="" class="main-body__news-comments-icon">22</p>
                        </div>
                    </div>
                </div>
            </a>
        </div>

        <div class="main-body__game-container">
            <a href="" class="main-body__game background_white">
                <img src="./img/Silent Hill f.png" alt="" class="main-body__game-icon">
                <div class="main-body__game-info">
                    <p class="main-body__game-name background_orange">Silent Hill f</p>
                    <p class="main-body__game-rating background_orange">Рейтинг 3.5</p>
                </div>
            </a>

            <div class="main-body__game-comments">
                <div class="main-body__game-comment-container background_white">
                    <img src="./img/AshBornd.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">AshBornd</p>
                        <p class="main-body__comment-content background_orange">Инди хоррор из steam за 200 рублей.</p>
                       <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="main-body__game-comment-container background_white">
                    <img src="./img/Alexander.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">Александр Матвейчук</p>
                        <p class="main-body__comment-content background_orange">Хорошая игра</p>
                       <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="main-body__game-comment-container background_white bottom-radius_15">
                    <img src="./img/GaryZhelezo.png" alt="" class="main-body__user-avatar">
                    <div class="main-body__game-comment">
                        <p class="main-body__username background_orange">GaryZhelezo</p>
                        <p class="main-body__comment-content background_orange">Хороший хоррор, средний соулс-лайк</p>
                        <div class="main-body__user-rating-container">
                            <div class="main-body__user-rating background_orange">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star active-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                                <img src="./icons/rateStar.svg" alt="" class="main-body__rate-star unactive-star">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer class="footer">
        <h1 class="footer__content">Футер</h1>
    </footer>
</template>

<style scoped>
     @font-face {
          font-family: "Rounded Mplus 1c Bold";
          src: url("./fonts/MPLUSRounded1c-Bold.ttf");

          font-family: "Rounded Mplus 1c Regular";
          src: url("./fonts/MPLUSRounded1c-Regular.ttf");
     }

     body {
          margin: 0;
          font-family: "Rounded Mplus 1c Bold";
          background-color: #DEDEDE;
          padding: 0;
     }

     .background_orange {
          background-color: rgba(255, 187, 115, 1);
     }

     .background_white {
          background-color: #F4EEE8;
     }

     .header {
          max-width: 1420px;
          width: 100%;
          height: 150px;
          display: flex;
          font-size: 35px;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          margin: 0px auto;
          gap: 20px;
          border-radius: 15px;
          padding: 0 10px;
     }

     .header__title {
          max-width: 324px;
          width: 100%;
          height: 100px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          border-radius: 41px;
          padding: 0 20px;
     }

     .header__logo {
          border-radius: 50%;
          width: 80px
     }

     .header__a {
          display: flex;
          justify-content: center;
          align-items: center;
          text-align: center;
          font-weight: bold;
          color: rgba(0, 0, 0, 1);
          text-decoration: none;
          background-color: rgba(255, 131, 0, 1);
          border-radius: 41px; 
          margin: 0px;
     }

     .header__title-a {
          max-width: 223px;
          width: 100%;
          height: 67px;
     }

     .header__nav {
          width: 710px;
          width: 100%;
          height: 100px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          border-radius: 41px;
          padding: 0 20px;
          gap: 20px;
     }

     .header__nav-a {
          max-width: 222px;
          width: 100%;
          height: 67px;
     }

     .header__search {
          max-width: 222px;
          width: 100%;
          height: 67px;
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
          padding: 0 auto;
     }

     .header__search-icon {
          max-width: 30px;
          width: 100%;
          margin-right: 10px;
     }

     .header__authorization {
          max-width: 400px;
          width: 100%;
          height: 100px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          border-radius: 41px;
          padding: 0 20px;
     }

     .header__authorization-a {
          max-width: 400px;
          width: 100%;
          height: 67px;
          padding: 0 10px;
     }

     .header__authorization-icon {
          max-width: 30px;
          width: 100%;
          margin-right: 10px;
     }

     .main-body {
          max-width: 1440px;
          width: 100%;
          /* height: 668px; */
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
          gap: 10px;
          margin: 0px auto;
          padding: 0 auto;
          flex-wrap: wrap;
     }

     .main-body__news-list {
          max-width: 860px;
          width: 100%;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          gap: 10px;
          margin: 0px;
     }

     .main-body__news {
          max-width: 860px;
          width: 100%;
          height: auto;
          display: flex;
          flex-direction: row;
          justify-content: space-around;
          padding: 12px 0px;
          text-decoration: none;
          color: black;
          font-family: "Rounded Mplus 1c Bold";
          font-weight: bold;
          font-size: 18px;
          border-radius: 15px;
          gap: 10px;
     }

     .main-body__news-img {
          margin: 0;
          padding: 0;
     }

     .main-body__news-info {
          max-width: 603px;
          width: 100%;
          height: 127px;
          display: flex;
          flex-direction: column;
          align-items: baseline;
          justify-content: center;
          gap: 17px;
     }

     .main-body__news-type {
          max-width: 132px;
          width: 100%;
          height: 26px;
          border-radius: 41px;
          margin: 0;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
     }

     .main-body__news-content {
          max-width: 590px;
          width: 100%;
          text-align: left;
          text-decoration: none;
          font-size: 17px;
          border-radius: 41px;
          margin: 0;
          padding: 5px 10px;
     }

     .main-body__news-rating-container {
          max-width: 590px;
          width: 100%;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          margin: 0px;
     }

     .main-body__news-rating {
          max-width: 132px;
          width: 100%;
          height: 26px;
          border-radius: 41px;
          margin: 0px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
     }

     .main-body__news-comments-container {
          max-width: 132px;
          width: 100%;
          height: 26px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          margin: 0px;
          border-radius: 41px;
          gap: 10px;
     }

     .main-body__news-comments {
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
     }

     .main-body__news-comments-icon {
          max-width: 22px;
          width: 100%;
          margin-right: 10px;
     }

     .main-body__game-container {
          max-width: 558px;
          width: 100%;
          height: 668px;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: space-between;
          gap: 10px;
          padding-top: 35px;
     }

     .main-body__game {
          max-width: 558px;
          width: 100%;
          height: 221px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          text-decoration: none;
          color: black;
          font-size: 35px;
          font-weight: bold;
          text-align: center;
          border-top-left-radius: 15px;
          border-top-right-radius: 15px;
          padding-top: 10px;
          padding-bottom: 10px;
     }

     .main-body__game-icon {
          max-width: 166px;
          width: 100%;
     }

     .main-body__game-info {
          max-width: 309px;
          width: 100%;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          gap: 31px;
     }

     .main-body__game-name {
          margin: 0px;
          text-decoration: underline;
          border-radius: 41px;
     }

     .main-body__game-rating {
          margin: 0px;
          border-radius: 41px;
     }

     .main-body__game-comments {
          max-width: 558px;
          width: 100%;
          height: 442px;
          display: flex;
          flex-direction: column;
          justify-content: baseline;
          gap: 5px;
     }

     .bottom-radius_15 {
          border-bottom-left-radius: 15px;
          border-bottom-right-radius: 15px;
     }

     .main-body__game-comment-container {
          max-width: 558px;
          width: 100%;
          height: 130px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-around;
          gap: 9px;
          margin: 0px;
     }

     .main-body__user-avatar {
          max-width: 69px;
          width: 100%;
          margin: 0px;
     }

     .main-body__game-comment {
          max-width: 430px;
          width: 100%;
          height: 116px;
          display: flex;
          flex-direction: column;
          gap: 9px;
     }

     .main-body__username {
          max-width: 192px;
          width: 100%;
          height: 19px;
          margin: 0;

          border-radius: 41px;
          font-size: 18px;
          font-weight: bold;
          text-align: center;
     }

     .main-body__comment-content {
          max-width: 430px;
          width: 100%;
          height: 65px;
          border-radius: 41px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: baseline;
          font-size: 22px;
          font-weight: bold;
          padding-left: 10px;
          margin: 0px;
     }

     .main-body__user-rating-container {
          max-width: 430px;
          width: 100%;
          height: 20px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: end;
     }

     .main-body__user-rating {
          max-width: 118px;
          width: 100%;
          height: 20px;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
          border-radius: 41px;
     }

     .unactive-star {
          opacity: 50%;
     }

     .footer {
          max-width: 1440px;
          width: 100%;
          height: 160px;
          border-radius: 15px;
          background: rgba(244, 238, 232, 1);
          margin: 0 auto;
          padding: 0;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
     }

     @media (max-width: 1458px) {
          .header {
               font-size: 18px;
               width: 880px;
               height: auto;
               gap: 5px;
               padding: 5px;
               padding-top: 5px;
               margin-bottom: 5px;
          }

          .header__nav, .header__title, .header__authorization{
               /* width: 70%; */
               padding: 5px;
               height: auto;
          }

          .header__authorization, .header__title, .header__authorization  {
               width: 60%;
               gap: 5px;
               margin: 0;
          }

          .header__nav-a, .header__search {
               width: 120px;
          }

          .header__nav {
               gap: 5px;
          }

          .main-body__news-list, .main-body__news, .main-body__game-container {
               max-width: 880px;
               padding: 5px;
          }
     }
</style>
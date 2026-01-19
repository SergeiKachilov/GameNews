<script setup>
     import NewsListItem from '@/components/NewsListItem.vue';
     import { onMounted, ref } from 'vue';
     import newsData from "@/components/json/news.json";
     const news_json = ref(newsData);

//     onMounted(() => {
//         fetch("src/components/json/news.json",)
//         .then((resp) => resp.json())
//         .then((json) => {
//             news_json.value = json;
//             console.log(json);
//         })
//     })
</script>

<template>
     <div class="main-body">
          <div class="news">
               <news-list-item v-for="news in news_json" class="news__item"
                          :news="news"
               ></news-list-item>
          </div>
     </div>
</template>

<style scoped>
     .main-body {
          display: flex;
          flex-direction: column;
          align-items: center;
     }
     .news {
          width: 80%;
          display: flex;
          flex-direction: column;
          gap: 1rem;
     }
     .news__item {
          /* font-size: 1.3rem; */
     }
</style>
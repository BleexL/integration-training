<template>
    <div class="article-list">
        <ul>
            <li v-for="article in articleList">
                <img :src="article.imageURL" :alt="article.title" />
                <div class="article-content">
                    <p class="article-number">{{ article.number }}</p>
                    <h2>{{ article.title }}</h2>
                    <p class="article-description">{{ article.description }}</p>
                </div>
            </li>
        </ul>
    </div>
</template>


<script setup>
    import newsHomepageTrendArticle from "/components/news-homepage/news-homepage-trend-article.vue"
    import { reactive } from 'vue';

    const articleList = reactive([
        {
        number: '01',
        imageURL:'/news-homepage-image-retro-pcs.jpg',
        title: "Reviving Retro PC's",
        description: "What happens when old PCs are given modern upgrades?"
        },
        {
        number: '02',
        imageURL:'/news-homepage-image-top-laptops.jpg',
        title: "Top 10 Laptops of 2022",
        description: "Our best picks for various needs and budgets."
        },
        {
        number: '03',
        imageURL:'/news-homepage-image-gaming-growth.jpg',
        title: "The Growth of Gaming",
        description: "how the pandemic has sparked fresh opportunities."
        }
    ]);
</script>


<style scoped>
    ul{
        margin: 0;
        padding: 0;
        list-style: none;
        display: flex;
        gap: 16px;
        width: 100%;
        /* flex-wrap: wrap; */
    }
    li{
        display: flex;
        height: 128px;
        gap: 24px;
        max-width: 50%;
    }
    .article-content{
        display: flex;
        flex-direction: column;
        gap: 8px;
    }
    .article-number{
        font-size: 32px;
        color: hsl(233, 8%, 79%);
        font-weight: 900;
        margin: 0;
        padding: 0;
        line-height: 32px;
    }
    h2{
        margin:0;
        padding: 0;
        font-size: 18px;
        line-height: 24px;

        transition: all 0.3s ease-in-out;
    }

    h2:hover{
        color: hsl(5, 85%, 63%);
    }
    .article-description{
        padding: 0;
        margin: 0;
    }
    @media screen and (max-width: 768px) {
        ul{
            flex-direction: column;
            width: 100%;
        }    
        li{
            max-width: 100%;
            min-height: 128px;
            height: auto;
        }
        img{
            width: 104px;
            height: auto;
            object-fit: cover;
        }
    }
</style>
<template>
    <div class="project-container">
        <div class="project-content">
            <news-homepage-header></news-homepage-header>
            <div class="first-section">
                <newsHomepageBigArticle class="big-article"/>
                <newsHomepageNewArticle class="new-artocle"/>
            </div>
            <newsHomepageTrendArticleList/>
        </div>
    </div>
</template>


<script setup>
import newsHomepageHeader from "/components/news-homepage/news-homepage-header.vue"
import newsHomepageButton from "/components/news-homepage/news-homepage-button.vue"
import newsHomepageBigArticle from "/components/news-homepage/news-homepage-big-article.vue"
import newsHomepageNewArticle from "/components/news-homepage/news-homepage-new-article.vue"
import newsHomepageTrendArticleList from "/components/news-homepage/news-homepage-trend-article-list.vue"


</script>


<style scoped>
    .project-container{
        background-color: #FEFDF9;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        display: flex;
        justify-content: center;
        width: 100%;
        height: auto;
        left: 0;
        top: 0;
        margin: 0;        
        overflow-y: hidden;;

    }
    .project-content{
        max-width: 1120px;
        margin-top: 32px;
        padding: 0px 32px;
        padding-bottom: 64px;
        display: flex;
        flex-direction: column;
        gap: 64px;
    }
    .first-section{
        display: flex;
        gap: 32px;
        width: 100%;
    }
    .big-article{
        max-width: 720px;
    }
    .new-article{
        width: 30%;
    }

    @media screen and (max-width: 1024px) {
        .first-section{
            flex-direction: column;
            gap: 64px;
        }
        .big-article{
            max-width: 1024px;
        }
    
    }
    @media screen and (max-width: 768px) {
        .project-container{
            padding: 0 16px;
            box-sizing: border-box;
            width: 100vw;
        }
        .project-content{
            padding: 0;
            width: 100%;
            padding-bottom: 40px;
        }
    }
</style>
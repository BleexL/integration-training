<template>
    <div class="component-container">
        <picture>
            <source media="(max-width: 768px)" srcset="/news-homepage-image-web-3-mobile.jpg">
            <img class="thumbnail" src="/news-homepage-image-web-3-desktop.jpg" alt="thumbnail the Bright Future of Web 3.0">
        </picture>
        
        <div class="content">
            <p class="title">The Bright Future of Web 3.0?</p>
            <div class="description-container">
                <p class="description-content">
                    We dive into the next evolution of the web that claims to put the power of the platforms back into the hands of the people. But is it really fulfilling its promise?
                </p>
                <newsHomepageButton>Read more</newsHomepageButton>
            </div>
        </div>
    </div>
</template>


<script setup>
import newsHomepageButton from "/components/news-homepage/news-homepage-button.vue"

</script>


<style scoped>
    .component-container{
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 32px;
    }
    .thumbnail{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .title{
        font-size: 56px;
        line-height: 56px;
        font-weight: 900;
        margin: 0;
        width: 50%;
    }
    .content{
        display: flex;
        font-size: 16px;
        line-height: 24px;
        gap: 32px;
    }
    .description-container{
        display: flex;
        flex-direction: column;
        gap: 32px;
        justify-content: center;
        width: 50%;
    }
    .description-content{
        margin: 0;
    }
    @media screen and (max-width: 1024px) {
        .component-container{
            flex-direction: row;
        }
        .content{
            flex-direction: column;
        }
        .thumbnail{
            width: 100%;
            max-height: 320px;
        }
        .title{
            width: 100%;
        }
        .description-container{
            width: 100%;
        }
    }
    @media screen and (max-width: 768px){
        .component-container{
            flex-direction: column;
        }
        .title{
            font-size: 40px;
        }
        .thumbnail{
            width: 100%;
        }
    }
</style>
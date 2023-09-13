<template>
    <div class="hero-container">
        <SunnysideHeader class="header"/>
        <div class="title">
            <h1>We are creatives</h1>
            <img src="/sunnyside-agency-landing-page/icons/icon-arrow-down.svg" alt="arrow down">
        </div>
    </div>
</template>


<script>
import SunnysideHeader from "/components/sunnyside/sunnyside-header.vue"
</script>


<style>
    .hero-container{
        background-image: url("/sunnyside-agency-landing-page/desktop/sunnyside-image-header.jpg");
        background-position: bottom;
        background-size: cover;
        width: 100vw;
        height: 100vh;

        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .header{
        position: absolute;
        top:0;
        left: 0;
    }
    .title{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    h1{
        font-family: Fraunces, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        color: white;
        font-size: 64px;
        text-transform: uppercase;
        letter-spacing: 8px;
    }

</style>
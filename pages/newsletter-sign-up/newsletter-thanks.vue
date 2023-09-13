<template>
    <div class="project-container">
        <div class="pop-up-container">
            <img src="/icon-success.svg" alt="icon success">
            <h1>Thanks for subscribing!</h1>
            <p>A confirmation email has been sent to your address. Please open it and click the button inside to confirm your subscription.</p>
            <nuxt-link to="/newsletter-sign-up/newsletter">
                <button class="cta-back">Dismiss message</button>
            </nuxt-link>        
        </div>
    </div>
</template>
<script setup>

</script>
<style scoped>
    .project-container{
        background-color: #242742;
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        position: fixed;
        left: 0;
        top: 0;
    }
    .pop-up-container{
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        background-color: white;
        /* display: flex;
        flex-direction: column; */
        border-radius: 32px;
        padding: 64px;
        color: #242742;
        width: 360px;
        box-shadow: 0px 4px 10px 0px rgba(17, 18, 29, 0.15);
    }
    h1{
        margin: 0;
        margin-top: 32px;
        margin-bottom: 24px;
        font-size: 56px;
        line-height: 56px;
    }
    p{
        margin: 0;
        margin-bottom: 16px;

        font-size: 16px;
        font-weight: 500;
    }    
    .cta-back{
        color: white;
        background-color: #242742;
        border: 0;
        border-radius: 8px;

        height: 48px;
        width: 100%;
        font-weight: bold;

        transition: all 0.2s ease-in-out;
    }

    @media screen and (max-width: 768px){
        .project-container{
            overflow: scroll;
            background-color: white;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: flex-end;
        }
        .pop-up-container{
            height: auto;
            width: 100%;
            border-radius: 0;
            padding: 0px 24px;
            box-shadow: none;
        }
        .cta-back{
            margin-top: 200px;
            margin-bottom: 40px;
        }
    }
</style>
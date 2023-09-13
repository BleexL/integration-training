<template>
    <div class="section">
        <div class="pop-up-container">
            <div class="left-side">
                <h1>Stay updated!</h1>
                <p>Join 60,000+ product managers receiving monthly updates on:</p>
                <ul>
                    <li>
                        <img src="/icon-list.svg" alt="icon list">
                        <p>Product discovery and building what matters</p>
                    </li>
                    <li>
                        <img src="/icon-list.svg" alt="icon list">
                        <p>Measuring to ensure updates are a success</p>
                    </li>
                    <li>
                        <img src="/icon-list.svg" alt="icon list">
                        <p>And much more!</p>
                    </li>
                </ul>
                <div class="cta-container">
                    <label for="email">Email address</label>
                    
                    <input type="text" id="email" name="email" placeholder="email@company.com" v-model="inputValue">
                    <!-- <a href="\pages\newsletter-sign-up\newsletter-thanks.vue">
                    </a> -->
                    <nuxt-link to="/newsletter-sign-up/newsletter-thanks">
                        <button :class="['subscribe-button', {active: inputValue}]">Subscribe to monthly newsletter</button>
                    </nuxt-link>
                </div>
            </div>
            <div class="right-side">
                <img class="desktop" src="/illustration-sign-up-desktop.svg" alt="decorative illustration">
                <img class="mobile" src="/illustration-sign-up-mobile.svg" alt="decorative illustration">
            </div>
        </div>
    </div>
</template>


<script setup>
import { ref } from 'vue';
import NewsletterThanks from "~/pages/newsletter-sign-up/newsletter-thanks.vue";
const inputValue = ref('');
</script>


<style scoped>
    .section{
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
        display: flex;
        border-radius: 32px;
        padding: 16px;
        color: #242742;
        width: 928px;
        box-shadow: 0px 4px 10px 0px rgba(17, 18, 29, 0.15);
        margin: 32px;
    }
    .left-side{
        padding: 64px;
        display: flex;
        flex-direction: column;
        gap: 24px;
    }
    h1{
        margin: 0;
        font-size: 52px;
        line-height: 56px;
    }
    p{
        margin: 0;
    
        font-size: 16px;
        font-weight: 500;
    }    
    ul{
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        flex-direction: column;
        gap: 8px;
    }
    li{
        display: flex;
        gap: 16px;
    }
    .cta-container{
        display: flex;
        flex-direction: column;
    }
    label{
        font-size: 12px;
        font-weight: bold;
        color: black;
        padding-bottom: 4px;
    }

    input{
        box-sizing: border-box;
        height: 48px;

        background-color: white;
        border: 1px solid rgba(36, 39, 66, 0.40);
        outline: none;

        padding: 0;
        padding-left: 16px;
        border-radius: 8px;
        margin-bottom: 16px;
    }

    input:focus{
        border: 1px solid rgba(36, 39, 66, 1);
    }

    .subscribe-button{
        color: white;
        background-color: #242742;
        border: 0;
        border-radius: 8px;

        height: 48px;
        width: 100%;
        font-weight: bold;

        transition: all 0.2s ease-in-out;
    }

    .subscribe-button.active{
        background: linear-gradient(90deg, #FF537B 0%, #FE693E 99.99%, rgba(255, 83, 123, 0.00) 100%);
        color: white;

    }
    .subscribe-button.active:hover{
        box-shadow: 0px 20px 40px 0px rgba(254, 94, 91, 0.45);
    }

    .mobile{
        display: none;
    }

    @media screen and (max-width: 768px) {
        .section{
            overflow: scroll;
            background-color: white;
            padding: 0;
        }
        .pop-up-container{
            height: 100%;
            width: 100vw;
            border-radius: 0;

            flex-direction: column-reverse;
            align-items: center;
            justify-content:flex-end;
            padding: 0;
            margin: 0;
        }
        .mobile {
            display: block;
            width: 100vw;
            max-width: 520px;
        }
        .desktop{
            display: none;
        }

        .left-side{
            padding: 24px;
        }
        h1{
            font-size: 52px;
        }

    }
</style>
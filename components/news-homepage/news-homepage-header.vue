<template>
    <div class="header-container">
        <nuxt-link to="">
            <img src="/news-homepage-logo.svg" alt="logo news homepage">
        </nuxt-link>
        <div class="mobile-menu" v-if="isMobile">
            <button class="overlay-button" @click="toggleOverlay">
                <img src="/news-homepage-icon-menu.svg" alt="button open menu">
            </button>
            <div class="overlay-container" v-if="showOverlay">
                <div class="overlay-content">
                    <button @click="toggleOverlay" class="overlay-button">
                        <img src="/news-homepage-icon-menu-close.svg" alt="Button to close the menu">
                    </button>
                    <ul class="overlay-list">
                        <li><nuxt-link to="">Home</nuxt-link></li>
                        <li><nuxt-link to="">New</nuxt-link></li>
                        <li><nuxt-link to="">Popular</nuxt-link></li>
                        <li><nuxt-link to="">Trending</nuxt-link></li>
                        <li><nuxt-link to="">Categories</nuxt-link></li>
                  </ul>
                </div>
            </div>
        </div>
        <ul v-else>
            <li><nuxt-link to="">Home</nuxt-link></li>
            <li><nuxt-link to="">New</nuxt-link></li>
            <li><nuxt-link to="">Popular</nuxt-link></li>
            <li><nuxt-link to="">Trending</nuxt-link></li>
            <li><nuxt-link to="">Categories</nuxt-link></li>
        </ul>
    </div>
</template>


<script setup>

import { ref, onMounted, defineProps, defineEmits } from 'vue';

// Variable pour stocker la dimension de l'écran
const screenWidth = ref(0); // Initialisé à 0

// Variable booléenne pour vérifier si l'écran est inférieur à 768px
const isMobile = ref(false); // Initialisé à false

// Fonction pour mettre à jour la dimension de l'écran
const updateScreenWidth = () => {
  if (typeof window !== 'undefined') { // Vérifie si window est défini
    screenWidth.value = window.innerWidth;
    isMobile.value = screenWidth.value < 768;
  }
};

// Écouter l'événement de redimensionnement de la fenêtre après le montage du composant
onMounted(() => {
  updateScreenWidth(); // Appel initial pour mettre à jour la taille de l'écran

  if (typeof window !== 'undefined') { // Vérifie à nouveau si window est défini
    window.addEventListener('resize', updateScreenWidth);
  }
});

// Retirer l'écouteur d'événement lorsque le composant est détruit (facultatif)
onBeforeUnmount(() => {
  if (typeof window !== 'undefined') { // Vérifie à nouveau si window est défini
    window.removeEventListener('resize', updateScreenWidth);
  }
});

// ------------------------- //

// Variable booléenne pour afficher/masquer l'overlay
const showOverlay = ref(false);

// Fonction pour basculer l'état de l'overlay
const toggleOverlay = () => {
  showOverlay.value = !showOverlay.value;
};

</script>


<style scoped>
    .header-container{
        display: flex;
        width: 100%;
        height: 40px;
        justify-content: space-between;
        align-items: center;
        
        color: hsl(236, 13%, 42%);
        font-weight: 400;

        position: relative;
    }
    ul{
        display: flex;
        flex-direction: row;
        list-style: none;
        gap: 16px;
    }
    li{
        transition: all 0.2s ease-in-out;
    }
    li:hover{
        color: hsl(5, 85%, 63%);
    }

    .overlay-container{
        width: 100vw;
        height: 100vh;

        position: absolute;
        left: -16px;
        top: -32px;

        background-color: rgba(0, 0, 0, 0.20);

        display: flex;
        justify-content: flex-end
    }
    .overlay-content{
        width: 66%;
        height: 100vh;

        background-color: white;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-end;

        padding: 16px;
        padding-top: 32px;
        box-sizing: border-box;

        gap: 64px;
    }
    .overlay-button{
        background-color: white;
        border: none;
        padding: 0;
        width: 40px;
        height: 40px;
    }
    .overlay-list{
        flex-direction: column;
        margin: 0;
        padding: 0;
        width: 100%;
        gap: 24px;

    }
    .overlay-list>li{
        width: 100%;
        font-size: 18px;
        font-weight: 500;
        line-height: 24px;
    }
   
</style>
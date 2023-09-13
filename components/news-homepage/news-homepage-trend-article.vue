<template>
    <div class="article-container">
        <img :src="imageURL" alt="Article thumbnail"/>
        <div>
            <p class="article-number">{{ number }}</p>
            <p class="article-title">{{ title }}</p>
            <p class="article-description">{{ description }}</p>
        </div>
    </div>
</template>


<script setup>
  const props = defineProps ({
    imageUrl: {
        type: String,
    },
    number: {
        type: Number,
    },
    title: {
        type: String,
    },
    description: {
        type: String,
    },
  })
</script>


<style scoped>
    
</style>
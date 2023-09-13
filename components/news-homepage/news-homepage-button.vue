<template>
    <div>
        <button>
            <slot></slot>
        </button>
    </div>
</template>


<script setup>

</script>


<style scoped>
    button{
        background-color: hsl(5, 85%, 63%);
        border: 0;
        color: white;
        text-transform: uppercase;
        letter-spacing: 4px;
        padding: 0px 32px;
        height: 48px;

        transition: all 0.3s ease-in-out;
    }
    button:hover{
        background-color: hsl(240, 100%, 5%);
    }
</style>
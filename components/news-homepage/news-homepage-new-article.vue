<template>
    <div class="component-container">
        <p class="title-section">New</p>
        <ul>
            <li>
                <p class="title-article">Hydrogen VS Electric Car</p>
                <p class="description-article">Will hydrogen-fueled cars ever catch up to EVs?</p>
            </li>
            <li>
                <p class="title-article">The Downsides of AI Artistry</p>
                <p class="description-article">What are the possible adverse effects of on-demand AI image generation</p>
            </li>
            <li>
                <p class="title-article">Is VC funding Dying Up?</p>
                <p class="description-article">Private Funding by VC firms is down 50% YOY. We take a look at what that means.</p>
            </li>
        </ul>
    </div>
</template>


<script setup>

</script>


<style scoped>
    .component-container{
        background-color: hsl(240, 100%, 5%);
        padding: 32px;
    }
    .title-section{
        color: hsl(35, 77%, 62%);
        font-weight: 700;
        font-size: 40px;
        margin: 0;
    }
    ul{
        list-style: none;
        color: white;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: column;
        gap: 16px;
    }
    li{
        display: flex;
        flex-direction: column;
        gap: 8px;
        padding: 32px 0px;
        border-bottom: 1px solid  hsl(236, 13%, 42%);
    }
    li:last-child{
        border: none;
        padding-bottom: 0;
    }
    li:first-child{
        padding-top: 16;
    }
    .title-article{
        margin: 0;
        padding: 0;
        font-size: 21px;
        font-weight: 600;
        line-height: 24px;
        
        transition: all 0.3s ease-in-out;
    }

    .title-article:hover{
        color: hsl(35, 77%, 62%);
    }

    .description-article{
        margin: 0;
        padding: 0;
        font-size: 16px;
        font-weight: 400;
        color: hsl(233, 8%, 79%);
    }

    @media screen and (max-width: 1024px) {
        ul{
            flex-direction: row;
        }
        li{
            border-bottom: 0;
            border-right: 1px solid hsl(236, 13%, 42%);
            width: 100%;
        }
    }
    @media screen and (max-width: 768px) {
        ul{
            flex-direction: column;
            width: 100%;
        }
        li{
            border-bottom: 1px solid hsl(236, 13%, 42%);
            border-right: 0;
            width: 100%;
        }
        .component-container{
            width: 100%;
            box-sizing: border-box;
            left: 0;
        }

    }
</style>
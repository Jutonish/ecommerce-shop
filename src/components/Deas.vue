<template>
    <div class="ideas">
        <HeroInformation
            title="It started with a small idea"
            description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
            background="#2A254B"
            colorTitle="#fff"
            colorDescription="#fff"
            :mobilePadding="true"
            />
        <img src="/src/assets/img/ImageBlock/Image Block.jpg" alt="" class="ideas-image">
    </div>
</template>

<script setup>

import HeroInformation from '@/components/HeroInformation.vue';

</script>

<style lang="sass" scoped>
.ideas
    display: grid
    grid-template-columns: repeat(2, 1fr)
    column-gap: 16px
    padding: 0 80px
    margin-bottom: 60px
    @media screen and (max-width: 767px)
        padding: 0
        grid-template-columns: 1fr
    &-image
        height: 100%
        width: 100%
        object-fit: cover
        @media screen and (max-width: 767px)

            padding: 0 24px
</style>
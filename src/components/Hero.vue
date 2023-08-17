<template>
    <div class="hero">
        <HeroInformation
        title="Luxury homeware for people who love timeless design quality"
        description="Shop the new Spring 2022 collection today"
        link="#"
        colorLink="lightgray"
        />
        <img class="hero-img" src="/src/assets/img/Hero1.png" alt="">
    </div>
</template>

<script setup>

import HeroInformation from '@/components/HeroInformation.vue';

</script>

<style lang="sass" scoped>

.hero
    background: url(/src/assets/img/Hero.jpg)
    height: 704px
    background-size: cover
    padding-right: 80px
    @media screen and (max-width: 767px)
        height: auto
        background: transparent
        padding-right: 0
        display: block
    &-img
        width: 100%

</style>
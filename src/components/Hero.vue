<template>
    <div class="hero">
        <HeroInformation
        title="Luxury homeware for people who love timeless design quality"
        description="Shop the new Spring 2022 collection today"
        link="#"
        />
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
    display: flex
    align-items: center
    justify-content: flex-end
    padding-right: 80px
    &-img
        min-width: 100%

</style>
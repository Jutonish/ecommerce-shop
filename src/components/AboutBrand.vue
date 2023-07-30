<template>
  <div class="about-brand">
    <h3 class="about-brand__title">What makes our brand different</h3>
    <div class="about-brand-elements">
        <div
            class="about-brand-element"
            v-for="(element, i) of aboutBrand"
            :key="i">
            <img 
                class="about-brand-element__img"
                :src="element.img"
                :alt="element.title"
            >
            <h4 class="about-brand-element__title">{{ element.title }}</h4>
            <span class="about-brand-element__description">{{ element.description }}</span>
        </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'

const aboutBrand = [
    {
        img: '/src/assets/svg/brend/Delivery.svg',
        title: 'Next day as standard',
        description: 'Order before 3pm and get your order the next day as standard'
    },
    {
        img: '/src/assets/svg/brend/Outline.svg',
        title: 'Made by true artisans',
        description: 'Handmade crafted goods made with real passion and craftmanship'
    },
    {
        img: '/src/assets/svg/brend/Purchase.svg',
        title: 'Unbeatable prices',
        description: 'For our materials and quality you wont find better prices anywhere'
    },
    {
        img: '/src/assets/svg/brend/Sprout.svg',
        title: 'Recycled packaging',
        description: 'We use 100% recycled to ensure our footprint is more manageable'
    },
]


</script>

<style lang="sass" scoped>

.about-brand
    padding: 80px 50px 130px 50px
    &-elements
        display: grid 
        grid-template-columns: repeat(4, 300px)
        justify-content: space-between
        @media screen and (max-width: 1024px)
            grid-template-columns: repeat(2, 1fr)
            gap: 20px
    &-element
        background: #F9F9F9
        padding: 49px
        &__img
            display: block
            margin-bottom: 12px
        &__title
            margin: 0 0 12px 0
            color: #2A254B
            font-size: 20px
        &__description
            font-size: 16px
            line-height: 1.5
    &__title
        text-align: center
        font-size: 24px
        color: #2A254B
        margin: 0 0 84px 0
</style>
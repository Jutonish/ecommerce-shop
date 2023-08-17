<template>
    <div 
        class="hero-info" 
        :style="{backgroundColor: background}" 
        :class="{'hero-info--mobile-padding': mobilePadding}">
        <div class="hero-info-text">
            <h2 
                class="hero-info-text__title"
                :style="{color: colorTitle}">{{ title }}</h2>
            <span 
                class="hero-info-text__description"
                :style="{color: colorDescription}">{{ description }}</span>
        </div>
        <ui-button 
            class="hero-info__btn"
            :mobileFullWidth="true" 
            :color="colorLink || 'secondary'" 
            type="link" 
            to="/">
            View collection
        </ui-button>
    </div>
</template>

<script setup>
import uiButton from '@/components/UI/Button.vue'
const props = defineProps({
    title: {
        type: String,
        required: false
    },
    description: {
        type: String,
        required: false
    },
    link: {
        type: String,
        required: false
    },
    colorTitle: {
        type: String,
        default: ''
    },
    colorDescription: {
        type: String,
        default: '#5B5676'
    },
    background: {
        type: String,
        default: '#fff'
    },
    colorLink: {
        type: String,
        required: false
    },
    mobilePadding: {
        type: Boolean,
        default: false
    },
})
</script>

<style lang="sass" scoped>

.hero
    &-info
        background: #fff
        max-width: 630px
        padding: 50px 0px 50px 55px
        min-height: 444px
        display: flex
        flex-direction: column
        justify-content: space-between
        align-items: flex-start
        @media screen and (max-width: 767px)
            min-height: 0
        &__btn
            @media screen and (max-width: 767px)
                margin: 32px 0
        &-text
            padding-bottom: 180px
            max-width: 450px
            @media screen and (max-width: 767px)
                padding-bottom: 12px
            &__title
                color: #22202E
                font-size: 32px
                @media screen and (max-width: 767px)
                    font-size: 18px
                    margin-bottom: 12px
            &__description
                color: #5B5676
                font-size: 18px
                @media screen and (max-width: 767px)
                    font-size: 11px
                    font-family: Satoshi
                    font-weight: 400
        &--mobile-padding
            @media screen and (max-width: 767px)
                padding: 26px 32px 0 26px
                margin: 0 24px 24px 24px

</style>
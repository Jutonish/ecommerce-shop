<template>
    <div class="hero-info" :style="{backgroundColor: background}">
       <div class="hero-info-text">
            <h2 
                class="hero-info__title"
                :style="{color: colorTitle}">{{ title }}</h2>
            <span 
                class="hero-info__description"
                :style="{color: colorDescription}">{{ description }}</span>
        </div>
        <ui-button :color="colorLink || 'secondary'" type="link" to="/">
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
        derault: ''
    },
    colorDescription: {
        type: String,
        derault: '#5B5676'
    },
    background: {
        type: String,
        derault: '#fff'
    },
    colorLink: {
        type: String,
        required: false
    }
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
        &-text
            padding-bottom: 180px
            max-width: 450px
            &__title
                color: #22202E
                font-size: 32px
            &__description
                color: #5B5676
                font-size: 18px
</style>
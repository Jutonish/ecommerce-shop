<template>
    <div class="subscribe">
        <div class="subscribe-content">
            <h3 class="subscribe-title">
                Join the club and get the benefits
            </h3>
            <span class="subscribe-description">
                Sign up for our newsletter and receive exclusive offers on<br>
                new ranges, sales, pop up stores and more
            </span>
            <div class="subscribe-checks">
                <div class="subscribe-check">
                    <img src="/src/assets/svg/login-footer/filled.svg"  height="24" width="24" alt="" class="subscribe-check__icon">
                    <span class="subscribe-check__name">Exclusive offers</span>
                </div>
                <div class="subscribe-check">
                    <img src="/src/assets/svg/login-footer/filled.svg"  height="24" width="24" alt="" class="subscribe-check__icon">
                    <span class="subscribe-check__name">Free events</span>
                </div>
                <div class="subscribe-check">
                    <img src="/src/assets/svg/login-footer/filled.svg"  height="24" width="24" alt="" class="subscribe-check__icon">
                    <span class="subscribe-check__name">Large discounts</span>
                </div>
            </div>
            <SubscribeForm />
        </div>
    </div>
</template>

<script setup>
import SubscribeForm from '@/components/SubscribeForm.vue'
</script>

<style lang="sass" scoped>

.subscribe
    background: url('/src/assets/img/login-footer/Image.jpg')
    background-size: cover
    padding: 97px 0 86px 0
    @media screen and (max-width: 767px)
        padding-top: 0
        padding-bottom: 0
    &-content
        min-width: 500px
        margin: auto
        text-align: center
        color: #fff
        @media screen and (max-width: 767px)
            padding: 24px 24px
            text-align: left
            width: 100%
    &-title
        margin: 0 0 12px 0
        font-size: 32px
        font-weight: 400
        @media screen and (max-width: 767px)
            font-size: 24px
    &-description
        font-size: 18px
        display: block
        margin-bottom: 30px
        @media screen and (max-width: 767px)
            font-size: 14px
    &-checks
        display: flex
        justify-content: center
        margin-bottom: 40px
        @media screen and (max-width: 767px)
            display: flex
            flex-direction: column
    &-check
        display: flex
        align-items: center
        &:nth-child(2)
            margin: 0 36px
        &__icon
            margin-right: 9px    
        @media screen and (max-width: 767px)
            &:nth-child(2)
                margin-left: 0
            padding-bottom: 9px
</style>
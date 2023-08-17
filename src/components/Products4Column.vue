<template>
    <div class="products-container">
        <div class="products">
            <Product
                v-for="product of products"
                :key="product.id"
                :img="product.img"
                :title="product.title"
                :price="product.price"/>
        </div>
        <div class="products-link">
            <ui-button :mobileFullWidth="true" color="lightgray" type="link" to="/">
                View collection
            </ui-button>
        </div>
    </div>
</template>

<script setup>
import Product from '@/components/Product.vue'
import {ref} from 'vue'
import uiButton from '@/components/UI/Button.vue'
const products = ref ([
	{
		id: 1,
		img: '/src/assets/img/products4column/Photo1.jpg',
		title: 'The Dandy chair',
		price: '£250'
	},
	{
		id: 2,
		img: '/src/assets/img/products4column/Photo2.jpg',
		title: 'Rustic Vase Set',
		price: '£150'
	},
	{
		id: 3,
		img: '/src/assets/img/products4column/Photo3.jpg',
		title: 'The Silky Vase',
		price: '£125'
	},
	{
		id: 4,
		img: '/src/assets/img/products4column/Photo4.jpg',
		title: 'The Lucy Lamp',
		price: '£399'
	},
])
</script>

<style lang="sass" scoped>
.products
    padding: 0 80px
    display: grid
    grid-template-columns: repeat(4, 1fr)
    column-gap: 20px
    margin-bottom: 65px
    @media screen and (max-width: 1024px)
        grid-template-columns: repeat(2, 1fr)
        row-gap: 20px
    @media screen and (max-width: 767px)
        padding: 0 24px
    &-container
        margin-bottom: 56px
    &-link
        text-align: center


</style>
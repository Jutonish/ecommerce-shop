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
        <div class="products-container-l">
            <button class="products-container-l__link">View collection</button>
        </div>
    </div>
</template>

<script setup>
import Product from '../components/Product.vue'
import {ref} from 'vue'

const products = ref ([
	{
		id: 1,
		img: '/src/assets/img/products4column/Photo1.jpg',
		title: 'The Dandy chair',
		price: 250
	},
	{
		id: 2,
		img: '/src/assets/img/products4column/Photo2.jpg',
		title: 'Rustic Vase Set',
		price: 150
	},
	{
		id: 3,
		img: '/src/assets/img/products4column/Photo3.jpg',
		title: 'The Silky Vase',
		price: 125
	},
	{
		id: 4,
		img: '/src/assets/img/products4column/Photo4.jpg',
		title: 'The Lucy Lamp',
		price: 399
	},
])
</script>

<style lang="sass" scoped>
.products
    padding: 0 80px
    display: flex
    grid-template-columns: repeat (4, 1fr)
    column-gap: 20px
    margin-bottom: 65px
    &-container
        margin-bottom: 56px
        &-l
            display: flex
            justify-content: center
            &__link
                padding: 16px 25px
                color: #2A254B
                width: 140px
                border: none
                &:hover
                    background: rgba(249, 249, 249, 0.35)

</style>
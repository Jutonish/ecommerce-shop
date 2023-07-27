<template>
	<header class="header">
		<div class="header-top">
			<div class="header-top-search">
				<img src="/src/assets/svg/head-search.svg" alt="search">
			</div>
			<router-link to="/" class="header-top-logo">Avion</router-link>
			<div class="header-top-right">
				<div class="header-top-right__cart">
					<router-link to="/cart">
						<img src="/src/assets/svg/head-cart.svg" alt="cart">
					</router-link>
				</div>
				<div class="header-top-right__avatar">
					<router-link to="/user">
						<img src="/src/assets/svg/head-avatar.svg" alt="user">
					</router-link>
				</div>
			</div>
		</div>
		<div class="header-menu">
			<router-link
				class="header-menu__link"
				:to="element.path"
				v-for="(element, i) of menu" 
				:key="i">{{ element.name }}
			</router-link>
		</div>
	</header>
</template>

<script setup>

import {ref} from 'vue'

const menu = [
	{
		name: 'Plant pots',
		path: '/plant'
	},
	{
		name: 'Ceramics',
		path: '/ceramics'
	},
	{
		name: 'Tables',
		path: '/tables'
	},
]

</script>

<style lang="sass" scoped>

.header
	height: 132px
	background: #fff
	&-top
		display: grid
		grid-template-columns: repeat(3, 1fr)
		height: 70px
		align-items: center
		border-bottom: 1px solid rgba(0, 0, 0, .1)
		margin: 0 28px
		&-right
			display: flex
			align-items: center
			justify-content: flex-end
			&__cart
				margin-right: 16px
		&-logo
			color: #22202E
			text-decoration: none
			font-size: 24px
			text-align: center
			&:hover
				text-decoration: underline
	&-menu
		height: 62px
		display: flex
		justify-content: center
		align-items: center
		&__link
			margin: 0 22px
			color: #726E8D
			text-decoration: none
			&:hover
				text-decoration: underline
</style>
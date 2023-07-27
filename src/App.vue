<template>
	<div class="container">
		<Header/>
		<Hero/>
		<AboutBrand/>
		<Products/>
		<Ideas/>
	</div>
  </template>

<script setup>
import Header from './components/layout/Header.vue'
import Hero from './components/Hero.vue'
import AboutBrand from './components/AboutBrand.vue'
import Products from './components/Products4Column.vue'
import Ideas from './components/Ideas.vue'
</script>

<style lang="sass">
@import url('https://fonts.cdnfonts.com/css/satoshi')

*
	box-sizing: border-box
	font-weight: 400

body
	margin: 0
	padding: 0
	font-family: 'Satoshi', sans-serif
	font-size: 16px

.container
	max-width: 1440px
	margin: auto

</style>

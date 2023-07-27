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
import Header from '@/components/layout/Header.vue'
import Hero from '@/components/Hero.vue'
import AboutBrand from '@/components/AboutBrand.vue'
import Products from '@/components/Products4Column.vue'
import Ideas from '@/components/Deas.vue'
</script>

<style lang="sass">
@import "./assets/style/global.sass"
</style>

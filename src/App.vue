<template>
	<div class="container">
		<Header/>
		<router-view />
		<Footer/>
	</div>
  </template>

<script setup>
import Header from '@/components/layout/Header.vue'
import Footer from '@/components/layout/footer.vue'
</script>

<style lang="sass">
@import "./assets/style/global.sass"
</style>

<template>
  <div class="page-wrapper">
  	<Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<style lang='sass'>

html
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif

*,
*::before,
*::after 
  box-sizing: border-box
  margin: 0

h2
  text-align: center


</style>

<script>
	import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
	export default{

	}
</script>
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


.page-wrapper
  width: 100%
  height: 100vh
  margin: 0
  display: flex
  flex-direction: column

h2
  text-align: center
  margin: auto

</style>

<script>
	import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
	export default{

	}
</script>
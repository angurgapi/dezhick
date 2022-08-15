<template>      
    <div class="navbar">
        <nuxt-link class="navbar__link" to="/">
           <font-awesome-icon :icon="['fas', 'home']" />about
        </nuxt-link>
       <nuxt-link class="navbar__link" to="/contacts">
           <font-awesome-icon :icon="['fas', 'envelope']" />contact
        </nuxt-link>
      </div>
</template>

<script>
	export default{
    name: 'Header',
    methods: {
      scrollToContact() {
        document.querySelector('#contact').scrollIntoView({behavior: 'smooth'})
      }
    },
	}
</script>

<style scoped lang='scss'>
.navbar {
  position: fixed;
  background-color: #dbd9cd;
  z-index: 1100;
  width: 100%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: row;
  padding: 20px 18px;
  box-shadow: 0 4px 6px -2px rgba(0,0,0,.3);
  font-size: 24px;
  @media(max-width: 800px) {
    font-size: 18px;
  }

  &__link {
    font-family: 'Zen';
    opacity: .5;
    color: #000;
    display: flex;
    align-items: center;
    font-size: 1.2rem;
    font-weight: 600;
    line-height: 1.2rem;
    margin-right: 10px;
    svg { 
     font-size: 1.2rem;
     line-height: 1.2rem;
     margin-right: 4px;  
    } 
   }

}


</style>
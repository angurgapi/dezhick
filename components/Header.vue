<template>      
    <div class="navbar">
        <nuxt-link to="/">
           <font-awesome-icon :icon="['fas', 'home']" />
        </nuxt-link>
        <button class="navbar__btn" @click="scrollToContact">Contact</button>
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
  padding: 20px 30px;
  box-shadow: 0 4px 6px -2px rgba(0,0,0,.3);
  &__btn {
    margin-left: 20px;
    text-decoration: none;
    font-family: 'Courier New';
    text-transform: uppercase;
    color: rgba(0,0,0,.7);
    font-size: 20px;
    line-height: 20px;
    font-weight: 300;
    margin-right: 20px;
  }
  .nuxt-link-exact-active {
    color: rgba(0,0,0,.5);
  }
}
.nuxt-link, .nuxt-link-active {
  text-decoration: none;
  color: rgba(0,0,0,.8);
}
svg { 
  font-size: 32px;
}
</style>
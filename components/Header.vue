<template>
  <div class="navbar">
    <nuxt-link class="navbar__link f-row" to="/">
      <font-awesome-icon :icon="['fas', 'home']" />
      <span>about</span>
    </nuxt-link>
    <nuxt-link class="navbar__link f-row" to="/contacts">
      <font-awesome-icon :icon="['fas', 'envelope']" />
      <span>contact</span>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    scrollToContact() {
      document.querySelector('#contact').scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>

<style scoped lang="scss">
.navbar {
  position: fixed;
  z-index: 1100;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: 20px 18px;
  width: 100%;
  height: 80px;
  box-shadow: 0 4px 6px -2px rgba(0, 0, 0, 30%);
  font-size: 24px;
  background-color: #dbd9cd;

  &__link {
    margin-right: 16px;
    height: 100%;
    font-family: 'Zen';
    font-weight: 600;
    color: #000;
    opacity: 0.5;
    transition: 0.4s all ease-in-out;

    span {
      font-size: 1.2rem;
    }

    svg {
      margin-right: 4px;
      font-size: 20px;
    }
  }

  @media (max-width: 800px) {
    font-size: 18px;
  }
}
</style>

<template>
  <div id="contact" class="contact">
    <div class="contact__box">
      <div class="contact__links">
        <a
          class="contact__link"
          target="_blank"
          href="https://www.instagram.com/dezhick/"
        >
          <font-awesome-icon
            class="contact__icon"
            :icon="['fab', 'instagram']"
          />
        </a>
        <a class="contact__link" target="_blank" href="https://t.me/dezhick">
          <font-awesome-icon
            class="contact__icon"
            :icon="['fab', 'telegram']"
          />
        </a>
        <a
          class="contact__link"
          target="_blank"
          href="mailto:dezhkoyulia@gmail.сom"
        >
          <font-awesome-icon
            class="contact__icon"
            :icon="['fas', 'envelope']"
          />
        </a>
      </div>
      <h4 class="contact__text">© Copyright Dezhick {{ getCurrentYear }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    getCurrentYear() {
      return new Date().getFullYear()
    }
  }
}
</script>

<style lang="scss" scoped>
.contact {
  background: linear-gradient(180deg, #dbd9cd, #5c5d5e);

  &__box {
    padding: 50px 20px 30px;
    width: 100%;
    text-align: center;
  }

  &__links {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__icon {
    border-radius: 4px;
    padding: 5px;
    font-size: 34px;
    color: #5c5d5e;

    &:not(last-child) {
      margin-right: 20px;
    }

    &:hover {
      color: #dbd9cd;
      background-color: #5c5d5e;
    }
  }

  &__text {
    margin-top: 30px;
    font-family: 'Zen';
    font-size: 22px;
    letter-spacing: 1px;
    color: #dbd9cd;
    opacity: 0.6;
  }
}
</style>

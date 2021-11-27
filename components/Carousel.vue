<template>
  <div class="carousel">
    <button class="carousel__button carousel__button--prev" @click="getPreviousSlide">
      <font-awesome-icon class="carousel__icon" :icon="['fas', 'arrow-circle-left']" />
    </button>
    <CarouserlSlide v-for="pic, index in section.pics" :key="pic.index" :pic="pic" :visible="index === activeSlide" />
    <button class="carousel__button carousel__button--next" @click="getNextSlide">
      <font-awesome-icon class="carousel__icon" :icon="['fas', 'arrow-circle-right']" />
    </button>
  </div>
</template>

<script>
import CarouserlSlide from './CarouselSlide.vue'

export default {
  name: 'Carousel',
  props: {
    section: {
      type: Object,
      required: true,
    },
  },
  components: {CarouserlSlide},

  data:() => ({
    activeSlide: 0,
  }),
  methods: {
    getPreviousSlide() {
      this.activeSlide > 0 ? this.activeSlide-- : this.activeSlide = this.section.pics.length -1
    },
    getNextSlide() {
      this.activeSlide < this.section.pics.length -1 ? this.activeSlide++ : this.activeSlide = 0 
    }
  },
}
</script>

<style lang="scss" scoped>
.carousel {
  display: flex;
  justify-content: center;
  &__button {
    position: relative;
    z-index: 1100;
    &--prev {
      right: -40px;
    }
    &--next {
      left: -40px;
    }
  }
  &__icon {
    color: #fff;
    background-color: rgba(0,0,0,.3);
    font-size: 30px;
    border-radius: 50%;
    box-shadow: 0 4px 6px -2px rgba(0,0,0,.3);
  }
}
</style>

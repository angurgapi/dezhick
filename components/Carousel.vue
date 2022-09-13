<template>
  <div class="carousel">
    <button
      class="carousel__button carousel__button--prev"
      @click="getPreviousSlide"
    >
      <font-awesome-icon
        class="carousel__icon"
        :icon="['fas', 'chevron-left']"
      />
    </button>
    <CarouserlSlide
      v-for="(pic, index) in section.pics"
      :key="pic.index"
      :pic="pic"
      :folder="section.slug"
      :visible="index === activeSlide"
    />
    <button
      class="carousel__button carousel__button--next"
      @click="getNextSlide"
    >
      <font-awesome-icon
        class="carousel__icon"
        :icon="['fas', 'chevron-right']"
      />
    </button>
  </div>
</template>

<script>
import CarouserlSlide from './CarouselSlide.vue'

export default {
  name: 'Carousel',
  components: { CarouserlSlide },
  props: {
    section: {
      type: Object,
      required: true
    }
  },

  data: () => ({
    activeSlide: 0
  }),
  methods: {
    getPreviousSlide() {
      this.activeSlide > 0
        ? this.activeSlide--
        : (this.activeSlide = this.section.pics.length - 1)
    },
    getNextSlide() {
      this.activeSlide < this.section.pics.length - 1
        ? this.activeSlide++
        : (this.activeSlide = 0)
    }
  }
}
</script>

<style lang="scss" scoped>
.carousel {
  display: flex;
  justify-content: center;
  position: relative;
  &__button {
    position: absolute;
    top: calc(50% - 23px);
    display: flex;
    flex-shrink: 0;
    justify-content: center;
    align-items: center;
    z-index: 1100;
    height: 46px;
    width: 46px;
    border-radius: 50%;
    border: none;
    box-shadow: 0 4px 6px -2px rgba(0, 0, 0, 0.3);
    background: #fff;

    @media (max-width: 800px) {
      height: 36px;
      width: 36px;
    }
    &:hover {
      opacity: 0.8;
    }

    &--prev {
      left: -4px;
    }
    &--next {
      right: -4px;
    }
  }
  &__icon {
    color: #5c5756;
    font-size: 30px;
    border-radius: 50%;
  }
}
</style>

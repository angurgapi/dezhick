<template>
  <div v-show="visible" class="carousel-slide">
    <img class="carousel-slide__img" :src="`/pics/${folder}/${pic}.jpg`" />
  </div>
</template>

<script>
export default {
  name: 'CarouselSlide',
  props: {
    pic: {
      type: [String, Number],
      required: true
    },
    folder: {
      type: String,
      required: true
    },
    visible: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({})
}
</script>

<style lang="scss" scoped>
.carousel-slide {
  display: flex;
  justify-content: center;
  &__img {
    min-width: 300px;
    max-width: 100%;
    max-height: 70vh;
  }
}
</style>

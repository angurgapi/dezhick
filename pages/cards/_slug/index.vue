<template>
  <div class="page-wrapper__content">
    <div class="section">
      <div class="section__header">
        <h2 ref="title" class="section__title">
          {{ getCurrentSection.title }}
        </h2>
      </div>
      <Carousel :section="getCurrentSection" />
    </div>
  </div>
</template>

<script>
import Carousel from '~/components/Carousel'

export default {
  components: {
    Carousel
  },

  data() {
    return {
      list: [
        {
          slug: 'joy',
          pics: [1, 2, 3, 4, 5, 6, 7, 8],
          title: 'JOY VIBE'
        },
        {
          slug: 'chill',
          pics: [1, 2, 3, 4, 5, 6],
          title: 'CHILL VIBE'
        },
        {
          slug: 'other',
          pics: [1, 2, 3, 4],
          title: '//OTHER'
        }
      ]
    }
  },
  computed: {
    getCurrentSection() {
      return this.list.filter(
        (section) => section.slug === this.$route.params.slug
      )[0]
    }
  }
}
</script>

<style scoped lang="scss">
.section {
  display: flex;
  flex-direction: column;
  align-items: center;

  // justify-content: center;
  padding: 20px;
  padding-top: 100px;
  height: 100%;

  &__header {
    height: 85px;
    font-family: 'Zen';
    font-size: 26px;
    letter-spacing: 3px;
  }

  &__pics {
    display: grid;
    grid-gap: 30px;
    grid-template-columns: repeat(2, 1fr);
    width: fit-content;

    @media (max-width: 700px) {
      grid-template-columns: 1fr;
    }
  }
}
</style>

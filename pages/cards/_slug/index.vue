<template>
    <div class="section">
      <div class='section__header'>
		  	<h2 class='section__title' ref='title'>{{ getCurrentSection.title }}</h2>			
		  </div>
      <Carousel :section="getCurrentSection" />
    </div>
</template>


<script>
import Carousel from '~/components/Carousel'


export default {
  components: {
    Carousel,
  },

  data(){
    return {
        list: [
        {
          slug: 'joy', pics: ['joy1', 'joy2'], title: 'JOY VIBE'
        },
        {
          slug: 'chill', pics: ['chill1', 'chill2', 'chill4', 'chill3'], title: 'CHILL VIBE'
        },
        {
          slug: 'other', pics: ['other1', 'other2', 'other3'], title: '//OTHER'
        }
      ],
    
    }
  },
  computed: {  	
    getCurrentSection() {
      return this.list.filter((section) => section.slug === this.$route.params.slug)[0]
    }
  }
}
</script>

<style scoped lang='scss'>
.section {
  height: 100%;
  padding-top: 100px;
  padding: 0 20px 20px 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  &__header {
    height: 85px;
    letter-spacing: 3px;
    font-family: 'Zen';
    font-size: 26px;
  }
  &__pics {
    width: fit-content;
    display: grid;
    grid-gap: 30px;
    grid-template-columns: repeat(2, 1fr); 
    @media(max-width: 700px) {
      grid-template-columns: 1fr;
    }
  }
}


</style>
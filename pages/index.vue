<template>
    <div class="intro">
      <div class="intro__header">
        <h2 class="festive">Oh hi there!</h2>
        <div class="intro__content">
          <img class="intro__image" src="/pics/gurl1.jpg" />             
          <div class="intro__text">
            <p>I figured you might come by. Later you may <a :href="`mailto:${email}`"><b>tell</b></a> me who you are, now I'm gonna tell you who I am. My name is Julia Dzezhko. 
            I was born and raised in Belarus, studied law and medicine and then got carried away with art. I think the point is to keep it simple & to remind y'all what actually makes our days. By now, I've spent a solid part of my life in Germany, living in various cities. You can imagine I've seen quite a lot...
            </p>
            <p style="margin-top: 20px">Now what would <b>YOU</b> like to see?</p>
          </div>
        </div>
      </div>
      <div class="grid">
        <div v-for="section in sections" :key="section.id" class="grid__item">
          <img :src="`/pics/${section.slug}cover.jpg`" />    
          <div class="middle" @click="goTo(section.slug)">
            <div class="middle__text">{{section.label}}</div>
          </div>     
        </div>
      </div>
    </div>
</template>



<script>
export default {
  data(){
    return {
      sections: [
        {
          id: 1, label: 'CHILL VIBE', slug: 'chill'
        },
        {
          id: 2, label: 'JOY VIBE', slug: 'joy'
        },
        {
          id: 3, label: '//OTHER', slug: 'other'
        }
      ],
      email: 'dezhkoyulia@gmail.сom'
    }
  },
  methods: {
    goTo(slug){
      this.$router.push(`/cards/${slug}`)
    }
},
}
</script>

<style lang='scss'>
.intro {
  margin-top: 150px;
  align-items: center;
  justify-content: center;
  padding: 20px; 
  &__header {
    display: flex;
    align-items: center;
    flex-direction: column;
  }
  &__content {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  &__image {
    height: 30vw;
    width: 30vw;
  }
  &__text {
    font-family: 'Zen';
    max-width: 25em;
    letter-spacing: 1px;
    text-align: justify;
    a {
      font-size: 26px;
      color: rgba(0,0,0,7);
      letter-spacing: 2px;
      text-decoration: underline;
      &:hover {
        color: rgba(0,0,0,4);
        text-decoration: none;
      }
    }
  }
}
.grid {
  width: fit-content;
  display: grid;
  grid-gap: 30px;
  grid-template-columns: repeat(3, 1fr);
  margin: 30px auto 40px;
  &__item {
    position: relative;
    &:hover img {
      opacity: 0.4;
    }
    &:hover .middle {
      opacity: 1;
    }
    box-shadow: 0 4px 6px -2px rgba(0,0,0,.3); 
    img {
      width: 25em;
      height: 25em;
      opacity: .2;
    }
    .middle {
      cursor: pointer;
      transition: .5s ease;
      opacity: 0.6;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      -ms-transform: translate(-50%, -50%);
      &__text {
        background-color: #fff;
        color: #000;
        font-size: 22px;
        padding: 16px 32px;
      }
    }
  }
}
@media(max-width: 1700px) {
  .wrapper {
    font-size: 16px;
  }
}

@media(max-width: 1300px) {

  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media(max-width: 1000px) {
    .wrapper {
    font-size: 12px;
  }
}
@media(max-width: 700px) {
  .intro__content {
    flex-direction: column;
  }
  .grid {
    grid-template-columns: 1fr;
    font-size: 14px;
  }
}
</style>
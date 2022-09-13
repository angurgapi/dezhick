<template>
  <div class="page-wrapper__content">
    <div class="contacts">
      <h2 class="festive">Get in touch</h2>
      <div class="contacts__main">
        <img src="pics/other/photo.jpg" />
        <div class="contacts__right f-column">
          <span>This is me, by the way.</span>
          <span>I'm avaliable on:</span>
          <div class="contacts__contact">
            <span>Instagram</span>
            <a target="_blank" href="https://www.instagram.com/dezhick"
              >https://www.instagram.com/dezhick
            </a>
          </div>
          <div class="contacts__contact">
            <span>Telegram</span>
            <a target="_blank" href="https://t.me/dezhick"> @dezhick </a>
          </div>
          <div class="contacts__contact">
            <span>E-mail</span>
            <a target="_blank" href="mailto:dezhkoyulia@gmail.сom">
              dezhkoyulia@gmail.сom
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.contacts {
  margin: auto;
  width: 100%;
  max-width: 600px;
  font-size: 16px;

  &__main {
    display: grid;
    align-items: center;
    grid-gap: 30px;
    grid-template-columns: 1fr 2fr;
    margin-top: 40px;

    img {
      border-radius: 50%;
      width: 12rem;
      height: 12rem;
    }

    span,
    a {
      font-family: 'Zen';
      font-size: 1.2rem;
    }

    a {
      color: rgba(0, 0, 0, 50%);
    }

    @media (max-width: 1000px) {
      justify-items: center;
      grid-template-columns: 1fr;
    }
  }

  &__right {
    width: 100%;
  }

  &__contact {
    display: grid;
    align-items: center;
    grid-gap: 18px;
    grid-template-columns: 40% 60%;

    @media (max-width: 600px) {
      grid-gap: 8px;
      grid-template-columns: 1fr;

      &:not(:first-child) {
        margin-top: 10px;
      }
    }
  }

  @media (max-width: 600px) {
    font-size: 12px;
  }
}
</style>

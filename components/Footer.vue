<template>
    <div class="contact" id="contact">
        <h2 class="festive">Get in touch</h2>
        <div class="contact__box">
            <div class="contact__links">
                <a class="contact__link" href="https://www.instagram.com/dezhick/">
                    <font-awesome-icon class="contact__icon" :icon="['fab', 'instagram']" />
                </a>
                <a class="contact__link" href="https://www.instagram.com/dezhick/">
                    <font-awesome-icon class="contact__icon" :icon="['fab', 'telegram']" />
                </a>
                <a class="contact__link" href="https://www.instagram.com/dezhick/">
                    <font-awesome-icon class="contact__icon" :icon="['fas', 'envelope']" />
                </a>
            </div>
            <h4 class="contact__text">© Copyright Dezhick 2021</h4>
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
.contact {    
  &__box {
    width: 100%;
    padding: 100px 20px 30px 20px;
    background: linear-gradient(180deg,#dbd9cd, #5c5d5e);
    text-align: center;

  }
  &__links {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &__icon {
      font-size: 34px;
      color: #5c5d5e;
      padding: 5px;
      border-radius: 4px;
      &:not(last-child) {
        margin-right: 20px;
      }
      &:hover {
          color: #dbd9cd;
          background-color: #5c5d5e;

      }
  }
  &__text {
      color: #dbd9cd;
      margin-top: 30px;
      font-family: 'Courier New';
      font-size: 22px;
      letter-spacing: 1px;
      opacity: .6;
  }
}
</style>
<template>
    <div class="page-wrapper__content">
        <div class="contacts">
         <h2 class="festive">Get in touch</h2>
         <div class="contacts__main">
             <img src="pics/other/photo.jpg" />
             <p>This is me, by the way</p>
         </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.contacts {
    margin: auto;
    width: fit-content;
    &__main {
        margin-top: 40px;
        display: flex;
        img {
            height: 250px;
            width: 250px;
            border-radius: 50%;
        }
        p {
            font-family: 'Zen';
        }
    }
}
</style>
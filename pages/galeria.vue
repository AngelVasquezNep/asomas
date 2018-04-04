<template lang="pug">
  #galeria
    .container
      .item.level-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img3.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img2.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img5.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img4.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/logo.png')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img4.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/logo.png')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img2.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img3.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img4.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/img5.jpg')", alt='a')
      .item.level-1
        img(v-lazy="require('~/assets/logo.png')", alt='a')



</template>

<script>
  export default {
    name: "Galeria",

    data() {
      return {
        rezised: 0,
        title: "Asomas | Galeria",
        description: "Galeria de Asomas"
      }
    },
    head () {
      return {
        title: this.title,
        meta: [
          { hid: 'description', name: 'description', content: this.description }
        ]
      }
    },

    mounted () {
      this.$bus.$emit('menu', 'galeria')
    }

  }
</script>

<style lang="sass" scoped>
#galeria
  margin-bottom: 40px  
.container
  display: grid
  grid-template-columns: repeat(4, 1fr)
  grid-gap: 10px
  justify-content: center
  grid-auto-flow: dense
  @media screen and (max-width: 768px)
    grid-template-columns: repeat(2, 1fr)
  @media screen and (max-width: 542px)
    grid-template-columns: 1fr

.item
  border-radius: 5px
  padding: 10px
  background-color: #ececec
  img
    max-width: 100%

.level-1
  grid-column-end: span 1

.level-2
  grid-column-end: span 2

.level-3
  grid-column-end: span 3

.level-4
  grid-column-end: span 4

.level-5
  grid-column-end: span 5
</style>

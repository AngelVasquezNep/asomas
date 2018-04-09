<template lang="pug">
  #galeria
    .container
      //- 540-960-6   -
      //- 720-248-1   -
      //- 720-960-8   - 2-2
      //- 960-548-10  - 3-1
      //- 960-897-2   - 3-2
      //- 960-720-3   - 3-2
      //- 960-720-5   - 3-2
      //- 960-720-7   - 3-2
      //- 960-720-9   - 3-2

      .item.column-2.row-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img2.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img3.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img5.jpg')", alt='a')
      .item.column-1.row-2
        img(v-lazy="require('~/assets/img6.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img7.jpg')", alt='a')
      .item.column-2.row-2
        img(v-lazy="require('~/assets/img8.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img9.jpg')", alt='a')
      .item.column-2.row-1
        img(v-lazy="require('~/assets/img10.jpg')", alt='a')
      .item.column-2
        img(v-lazy="require('~/assets/img1.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img2.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img3.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img5.jpg')", alt='a')
      .item.column-1.row-1
        img(v-lazy="require('~/assets/img6.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img7.jpg')", alt='a')
      .item.column-2.row-2
        img(v-lazy="require('~/assets/img8.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img9.jpg')", alt='a')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img10.jpg')", alt='a')



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
  // align-items: center
  display: grid
  grid-template-columns: repeat(6, 1fr)
  grid-gap: 5px
  justify-content: center
  grid-auto-flow: dense
  @media screen and (max-width: 768px)
    grid-template-columns: repeat(1, 1fr)
    .column-2, .column-3, .column-4, .column-5, .column-6
      grid-column-end: span 1
    .row-2, .row-3, .row-4, .row-5, .row-6
      grid-row-end: span 1

.item
  border-radius: 5px
  padding: 10px
  background-color: #f4f4f4
  img
    max-width: 100%

.column-1
  grid-column-end: span 1

.column-2
  grid-column-end: span 2

.column-3
  grid-column-end: span 3

.column-4
  grid-column-end: span 4

.column-5
  grid-column-end: span 5

.row-1
  grid-row-end: span 1

.row-2
  grid-row-end: span 2

.row-3
  grid-row-end: span 3


</style>

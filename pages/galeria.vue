<template lang="pug">
  #galeria
    .container
      .item.column-2.row-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img2.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img3.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img5.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img7.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img9.jpg')", alt='asomas')
      .item.column-2.row-1
        img(v-lazy="require('~/assets/img10.jpg')", alt='asomas')
      .item.column-2
        img(v-lazy="require('~/assets/img1.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img2.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img3.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img5.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img7.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img9.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img10.jpg')", alt='asomas')
      .item.column-2.row-1
        img(v-lazy="require('~/assets/img1.jpg')", alt='asomas')
      .item.column-3.row-2
        img(v-lazy="require('~/assets/img2.jpg')", alt='asomas')



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
  align-items: center
  display: grid
  grid-template-columns: repeat(auto-fill, 300px)
  grid-gap: 5px
  justify-content: center
  @media screen and (max-width: 600px)
    grid-template-columns: 1fr
    margin: 5px

.item
  border-radius: 5px
  padding: 10px
  background-color: #f4f4f4
  transition: .5s all
  &:hover
    background-color: #00CDB3
  img
    max-width: 100%



</style>

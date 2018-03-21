<template lang="pug">
  #galeria
    .container
      .item.level-2
        img(src='~/assets/img1.jpg', alt='')
      .item.level-2
        img(src='~/assets/img3.jpg', alt='')
      .item.level-2
        img(src='~/assets/img1.jpg', alt='')
      .item.level-1
        img(src='~/assets/img2.jpg', alt='')
      .item.level-1
        img(src='~/assets/img5.jpg', alt='')
      .item.level-1
        img(src='~/assets/img4.jpg', alt='')
      .item.level-2
        img(src='~/assets/logo.png', alt='')
      .item.level-1
        img(src='~/assets/img4.jpg', alt='')
      .item.level-2
        img(src='~/assets/logo.png', alt='')
      .item.level-1
        img(src='~/assets/img1.jpg', alt='')
      .item.level-1
        img(src='~/assets/img2.jpg', alt='')
      .item.level-1
        img(src='~/assets/img3.jpg', alt='')
      .item.level-1
        img(src='~/assets/img4.jpg', alt='')
      .item.level-1
        img(src='~/assets/img5.jpg', alt='')
      .item.level-2
        img(src='~/assets/logo.png', alt='')
</template>

<script>
  export default {
    name: "Galeria"
  }
</script>

<style lang="sass" scoped>
#galeria
  margin-bottom: 40px  
.container
  display: grid
  grid-template-columns: repeat(auto-fill, 200px)
  grid-gap: 10px
  justify-content: center
  grid-auto-flow: dense

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

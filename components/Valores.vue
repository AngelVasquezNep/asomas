<template lang="pug">
  .valores-slot
    slot(name="title")
      h3
    slot(name="imagen")
      img(src="")
    slot(name="description")
      p
</template>

<style lang="sass" scoped>
.valores-slot
  transition: .3s
  // border: 1px solid #FFA500
  h3
    color: #FF003C
  img
    margin: 5px
    width: 90%
  p 
   line-height: 30px
   font-weight: normal
  &:hover 
      transform: scale(1.06) translateY(-5px)
      box-shadow: 0 0px 0px 4px #9c9c9c
      box-shadow: 0 0px 0px 6px #00CDB3
</style>

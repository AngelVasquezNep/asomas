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
  // border: 1px solid #FFA500
  h3
    color: #FF003C
  img
    margin: 5px
    width: 90%
  p 
   line-height: 30px
   font-weight: normal
</style>

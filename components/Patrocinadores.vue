<template lang="pug">
  #patrocinadores
    .slider
      ul
        li
          img( src="~/assets/img1.jpg", alt="Imagen1")
        li
          img( src="~/assets/img1.jpg", alt="Imagen2")
        li
          img( src="~/assets/img1.jpg", alt="Imagen3")
        li
          img( src="~/assets/img1.jpg", alt="Imagen4")


</template>

<script>
  export default {
    name: 'Patrocinadores'
  }
</script>

<style lang="sass" scoped>


.slider 
  width: 100%
  margin: 0
  overflow: hidden


.slider ul 
  display: flex
  padding: 0
  width: 400%
  
  animation: cambio 20s infinite alternate linear


.slider li 
  border: 1px solid red
  list-style: none
  display: grid
  width: 100%
  justify-content: center


.slider img 
  width: 100%


@keyframes cambio 
  0% 
    margin-left: 0
  10% 
    margin-left: 0
  
  20% 
    margin-left: -100%
  45% 
    margin-left: -100%
  
  55% 
    margin-left: -200%
  80% 
    margin-left: -200%
  
  90% 
    margin-left: -300%
  100% 
    margin-left: -300%



</style>

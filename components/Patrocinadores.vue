<template lang="pug">
  #patrocinadores
    .subtitle.centrar
      h2 Patrocinadores 
    .slider
      ul
        li
          picture
            img( src="~/assets/patrocinadores/camsa.png", title="Camsa" ,alt="Camsa")
        li
          picture
            img( src="~/assets/patrocinadores/casamaria.png", title="Casa Maria" ,alt="Casa Maria")
        li
          picture
            img( src="~/assets/patrocinadores/casanovarent.jpg", title="casanovarent" ,alt="casanovarent")
        li
          picture
            img( src="~/assets/patrocinadores/grupopakar.svg", title="grupopakar" ,alt="grupopakar")
        li
          picture
            img( src="~/assets/patrocinadores/invex.png", title="Invex" ,alt="Invex")
        li
          picture
            img( src="~/assets/patrocinadores/kesmeralda.png", title="kesmeralda" ,alt="kesmeralda")
        li
          picture
            img( src="~/assets/patrocinadores/KPMG.png", title="KPMG" ,alt="KPMG")
        li
          picture
            img( src="~/assets/patrocinadores/mahen.png", title="Mahen" ,alt="Mahen")
        li
          picture
            img( src="~/assets/patrocinadores/movistar.png", title="Movistar" ,alt="Movistar")
        li
          picture
            img( src="~/assets/patrocinadores/nmp.png", title="NMP" ,alt="NMP")
        li
          picture
            img( src="~/assets/patrocinadores/perkins.png", title="Perkins" ,alt="Perkins")
        li
          picture
            img( src="~/assets/patrocinadores/proteccion.png", title="Proteccion" ,alt="Proteccion")
        li
          picture
            img( src="~/assets/patrocinadores/rich.png", title="Rich" ,alt="Rich")
        li
          picture
            img( src="~/assets/patrocinadores/sas.jpg", title="SAS" ,alt="SAS")


</template>

<script>
  export default {
    name: 'Patrocinadores'
  }
</script>

<style lang="sass" scoped>
#patrocinadores
  margin: 40px 0

.subtitle
  background-color: #FF003C
  color: #fff
  padding: 20px 0
  margin: 20px 0
  font-size: 2em


.slider 
  width: 100%
  margin: 0
  // overflow: hidden
  background-color: rgb(0, 149, 183)
  width: 1400% 

  &:hover ul
    animation-play-state: paused

.slider ul 
  display: flex
  padding: 0

  animation: cambio 40s infinite alternate linear



.slider li 
  list-style: none
  display: grid
  // width: 100%
  // width: 300px
  // justify-content: center
  align-items: center

.slider picture
  // width: 200px
  padding: 10px
.slider img 
  width: 100%


@keyframes cambio 
  0% 
    margin-left: 0
  2% 
    margin-left: 0
  
  // 20% 
  //   margin-left: -10%
  // 45% 
  //   margin-left: -10%
  
  // 55% 
  //   margin-left: -20%
  // 80% 
  //   margin-left: -20%
  
  98% 
    margin-left: -24%
  100% 
    margin-left: -24%



</style>

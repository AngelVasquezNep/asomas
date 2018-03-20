<template lang="pug">
.asomas
  #inicio.logo.centrar
    picture
      img(src='~/assets/logo.png', alt='')
  .container
    .item.portada.centrar
      h1.mensaje-portada ¡Asomate a su mundo y descubré todas las maravillas que existen!
    .item.descripcion.centrar
      p
        span ASOMAS
        |  es una Institución de Asistencia Privada sin fines de lucro 
        span
          | que tiene la misión de fomentar el desarrollo integral de personas sordociegas y/o con discapacidad múltiple
        |  con el fin de lograr una inclusión a nivel familiar, social, escolar y laboral.
    .item.video.centrar
      iframe(width='627', height='353', src='https://www.youtube.com/embed/eKLl-2sHLG0', frameborder='0', allow='autoplay; encrypted-media', allowfullscreen='')
    .item.banner.centrar
      .imagen-banner.centrar
        img(src='~/assets/img1.jpg', alt='')
    .item.mensaje-motivacion.centrar
      p ¡Vamos a cambiar el mundo con tu ayuda!
    .item.fotos-principales.centrar
      img(src='~/assets/img2.jpg', alt='')
      img(src='~/assets/img3.jpg', alt='')
      img(src='~/assets/img4.jpg', alt='')
      img(src='~/assets/img5.jpg', alt='')
    .item.valores.centrar
      .valores-container
        h2 Nuestros Valores
        ul.centrar
          li  Respeto
          li  Dignidad
          li  Calidez
          li  Familia
          li  Aceptación
          li  Colaboración
          li  Honestidad
          li  Transparencia.
    .item.centrar.logros-principales
      .logros-principales-container
        h2 Enterate de algunos de nuestros logros 
        ul.centrar
          li  Incrementar el número de alumnos atendidos de 3 a 34 en el Programa Básico. 
          li Desarrollar instrumentos de diagnóstico, evaluación y seguimiento del avance de los alumnos.
          li Brindar diplomados reconocidos de manera oficial en diversas entidades federativas.
          li  ¡Y la lista sigue!
        p Estamos seguros que quieres ser parte de este gran proyecto así que aprieta el botón y descubre la magia
        .btn
          router-link(to='/apoyo') Quiero ver la magia
    
    .item.mision-vision
      Mision
    .item.patrocinadores
      Patrocinadores  
    .item.mision-vision
    
  
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import Mision from '~/components/Mision.vue'
import Patrocinadores from '~/components/Patrocinadores.vue'

export default {
  name: "index",
  components: { AppLogo, Mision, Patrocinadores },
  methods: {
    
    
  }
}
</script>

<style lang="sass" scoped>
*
  margin: 0
  padding: 0

\:root
  --main-color: #00CDB3
  --second-color: #FFA500
  --red-color: #FF003C
  --height-menu: 50px

body
  margin: 0
  font-family: 'Montserrat', sans-serif
  overflow-x: hidden

ul
  list-style: none

a
  height: inherit
  text-decoration: none
  color: #000

.centrar
  display: flex
  justify-content: center
  align-items: center
  text-align: center
  flex-direction: column



.logo
  margin: 80px 0 30px 0

.container
  display: grid
  grid-template-columns: repeat(4, 1fr)
  min-height: 100vh
  justify-content: center
  overflow-x: hidden


.item
  display: flex
  justify-content: center
  align-items: center

.portada
  grid-area: portada
  grid-column: 1 / -1

.mensaje-portada
  color: rgb(3, 170, 148)
  text-align: center
  font-size: 4em
  padding: 40px 0

.descripcion
  text-align: end
  grid-column: span 2
  p
    padding: 15px
    font-size: 20px
    line-height: 50px
  span
    font-size: 2em
    color: #fff
    background-color: var(--main-color)
    &:nth-of-type(2)
      font-size: 1.1em
      color: #fff
      background-color: var(--second-color)

.video
  grid-column: span 2
  padding: 30px 0
  iframe
    width: 100%

.mensaje-motivacion
  height: 200px
  grid-column: 1 / -1
  position: relative
  font-size: 4em
  color: var(--main-color)
  p
    transform: rotate(-1deg)

.banner
  grid-column: 1 / span 4
  width: 100%
  .imagen-banner
    width: 100%
    img
      width: 90%

.fotos-principales
  grid-column: 1 / -1
  padding: 40px 10px
  display: grid
  grid-template-columns: repeat(auto-fill, 250px);
  grid-gap: 10px
  justify-content: center
  justify-items: center
  img
    width: 100%
    transition: .3s
    &:hover
      box-shadow: 8px 8px var(--red-color)

.valores
  font-size: 1.1em
  display: block
  line-height: 55px
  font-weight: bold
  box-sizing: border-box
  ul
    display: block
  .valores-container
    transition: .2s
    margin: 0 10px
    height: 100%
    border: 1px solid var(--main-color)
  h2
    font-size: 2em
    color: var(--second-color)
  .valores-container:hover
    box-shadow: 8px 8px var(--main-color)

.logros-principales
  grid-column: span 3
  font-size: 1.29em
  line-height: 50px
  transition: .3s
  .centrar
    flex-direction: column
  h2
    color: var(--main-color)
    font-size: 2em
    padding: 10px
  li
    &:nth-of-type(2n - 1)
      transform: rotate(0.5deg)
      color: var(--red-color)
    &:nth-of-type(2n)
      transform: rotate(-0.5deg)
      color: #fff
      background: rgba(178, 8, 201, 0.925)
  p
    font-size: 1.2em
    color: var(--second-color)
    font-weight: bold

  &:hover
    transform: translateY(-5px)
    box-shadow: 0 3px 10px 2px #9c9c9c

.mision-vision
  grid-column: 1 / -1

.patrocinadores
  grid-column: 1 / -1



.btn
  margin: 25px auto
  width: 90%
  border: 3px solid var(--red-color)
  border-radius: 10px
  transition: .5s
  outline: none
  a
    display: block
    transition: .5s
    font-weight: bold
    color: #fff
    color: var(--red-color)
    font-size: 1.3em
    width: 100%
    height: 100%
  &:active
    transform: scale(0.98)

</style>

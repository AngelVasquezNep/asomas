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
    .item.valores
      h2 Nuestros Valores
      .valores-container
        Valores
          img(slot="imagen" src="~/assets/valores/respeto.png", alt="respeto")
          h3(slot="title") Respeto
          p(slot="description") Respeto a la dignidad de las personas con discapacidad y sus familias.
        Valores
          img(slot="imagen" src="~/assets/valores/dignidad.png", alt="dignidad")
          h3(slot="title") Dignidad
          p(slot="description") Dignidad para cada ser humano.
        Valores
          img(slot="imagen" src="~/assets/valores/calidez.png", alt="calidez")
          h3(slot="title") Calidez
          p(slot="description") Calidad y calidez de la atención.
        Valores
          img(slot="imagen" src="~/assets/valores/integracio.png", alt="familia")
          h3(slot="title") Integración
          p(slot="description") Integración del alumno y la familia por medio de oportunidades y experiencias funcionales. 
        Valores
          img(slot="imagen" src="~/assets/valores/aceptacion.png", alt="aceptacion")
          h3(slot="title") Aceptación
          p(slot="description") Aceptación de diferentes ideologías, religiones, sexos, razas o grupos sociales.
        Valores
          img(slot="imagen" src="~/assets/valores/colaboracion.png", alt="colaboracion")
          h3(slot="title") Colaboración
          p(slot="description") Colaboración con otras instituciones con objetivos afines en beneficio de las personas con sordoceguera y/o retos múltiples.
        Valores
          img(slot="imagen" src="~/assets/valores/honestidad.png", alt="honestidad")
          h3(slot="title") Honestidad
          p(slot="description") Honestidad para cada miembro de Asomas y del mundo.
        Valores
          img(slot="imagen" src="~/assets/valores/transparencia.png", alt="transparencia")
          h3(slot="title") Transparencia
          p(slot="description") Transparencia en cada acto y decisión.
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
import Valores from '~/components/Valores.vue'

export default {
  name: "index",
  components: { AppLogo, Mision, Patrocinadores, Valores },
  
  data() {
    return {
      title: "Asomas ",
      description: "Home de Asomas"
    }
  },
  
  head () {
    return {
      title: this.title,
      meta: [
        { hid: 'description', name: 'description', content: this.description }
      ]
    }
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
  width: 100%
  margin: 80px 0 30px 0
  img
    width: 100%

.container
  display: grid
  grid-template-columns: repeat(4, 1fr)
  min-height: 100vh
  justify-content: center
  overflow-x: hidden
  @media screen and (max-width: 768px)
    grid-template-columns: 1fr 1fr
    .mensaje-portada, .video, .logros-principales, .valores
      grid-column: 1 / -1
    .video
      width: 80%
      margin: auto
    .fotos-principales
      grid-template-columns: 1fr 1fr
    .logros-principales
      padding: 20px
      margin: 20px 0
    .mensaje-motivacion
      font-size: 2.5em
  @media screen and (max-width: 544px)
    .fotos-principales
      grid-template-columns: 1fr 
    .video 
      width: 95%
    .banner
      img
        width: 100% !important

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
  grid-column: 1 / -1
  width: 100%
  .imagen-banner
    width: 100%
    img
      width: 90%

.fotos-principales
  grid-column: 1 / -1
  padding: 40px 10px
  display: grid
  grid-template-columns: repeat(4, 1fr);
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
  line-height: 55px
  font-weight: bold
  box-sizing: border-box
  grid-column: 1 / -1
  display: flex
  flex-direction: column
  text-align: center
  margin: 10px
  .valores-container
    padding: 10px
    display: grid
    justify-content: space-evenly
    width: 90%
    grid-template-columns: repeat(auto-fill, 250px)
    grid-gap: 25px
    transition: .2s
    // border: 1px solid var(--main-color)
    
  h2
    font-size: 2em
    margin: 20px auto
    color: var(--second-color)
  .valores-container:hover
    // box-shadow: 8px 8px var(--main-color)

.logros-principales
  grid-column: 1 / -1
  font-size: 1.29em
  line-height: 50px
  transition: .3s
  margin: 10px
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
  &:hover
    background-color: var(--red-color)
    a
      color: #fff
  &:active
    transform: scale(0.98)

</style>

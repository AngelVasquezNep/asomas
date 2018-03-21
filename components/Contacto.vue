<template lang="pug">
  #contacto.item.centrar.contacto
      .mapa-google
        iframe(src='https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15048.4652477523!2d-99.20694841968754!3d19.450551424528683!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85d2023beac1c209%3A0x81ffd020bdf89566!2sAsomas!5e0!3m2!1ses-419!2smx!4v1519986215454', width='500', height='300', frameborder='0', style='border:0', allowfullscreen='')
      h3.centrar.contacto-frase Siempre puedes contar con nosotros
      .centrar.telefonos
        p
          | contacto@asomas.org.mx
        p
          | (55) 53957679
          | (55) 55803397
          | Ext 101
      .centrar.direccion
        | Retorno Miguel Lanz Duret # 57
        | Col. Periodista
        | Del. Miguel Hidalgo
        | CP: 11220
        | RFC: AMA0111218G0
      .centrar.facebook
        a.centrar(href="https://www.facebook.com/Asomas-IAP-127976263916799/" target="_blank") 
          img.logoface(src="~/assets/facebook.svg")
      .centrar.design-by
        p Diseñado por Ángel Vásquez 
        a.centrar(href="https://www.github.com/angelvasqueznep" target="_blank") 
          p Github 
            img.github(src="~/assets/github.svg")
</template>

<script>
  export default {
    name: 'Contacto'
  }
</script>

<style lang="sass" scoped>
.contacto
  display: grid
  padding-top: 30px
  border-top: 2px dashed #00CDB3
  grid-gap: 5px
  grid-template-columns: repeat(3, 1fr)
  grid-template-rows: 1fr 1fr 40px
  grid-column: 1 / -1
  > *
    height: inherit
  a
    color: #000
    text-decoration: none
  .contacto-frase
    line-height: 50px
    color: #fff
    transform: rotate(-5deg)
    background-color: #FFA500
  .telefonos
    color: #fff
    line-height: 50px
    font-size: 19px
    height: 100%
    background-color: #00CDB3
  .mapa-google
    grid-row: span 3
  .facebook
    .logoface
      width: 60%
  .design-by
    font-size: 1.1em
    color: #fff
    height: 100%
    grid-column: span 2
    background-color: #FF003C
    display: grid
    grid-template-columns: 1fr 1fr
    .github
      width: 20px

  @media screen and (max-width: 870px)
    grid-template-columns: 2fr
    grid-gap: 20px
    .contacto-frase
      transform: rotate(0)

    .design-by
      grid-column: 1
      padding: 10px 0
    .facebook
      .logoface
        width: 30%


</style>

<template lang="pug">
  #apoyo.centrar
    hgroup
      h1 ¡Nos encanta saber que quieres apoyar!
      h2 ¡Asomate a nuestro mundo!
      h3 Tu apoyo es lo más valioso
    .descripcion.centrar
      p Hay muchas formas en las que puedes ayudar, puede ser en efectivo, en especie, artículos de papeleria, 
      |
      span ¡Puedes hacer tu servicio social! 
      | o 
      span ¡Ser voluntario! 
      p Nos encantaría tenerte por aquí.

    section.donativos
      h2 DONATIVOS EN EFECTIVO
      
      .efectivo
        
        p Los cuales van directamente en aumentar cuantitativa y cualitativamente los servicios que apoyan la rehabilitación de los niños jóvenes y familias que asisten a ASOMAS:
        
        p  Asociación Mexicana Anne Sullivan IAP
        p  BBVA Bancomer
        p  Cta: 0136596258
        p  CLABE: 012 1800 01365962583

        p DONATARIA AUTORIZADA 2017
        p DOF : Lunes 9 de Enero 2017

      h2 DONATIVOS EN ESPECIE DE PRODUCTOS ESPECÍFICOS
      
      .item
        h3 ARTÍCULOS DE LIMPIEZA
        ul
          li Cloro
          img(src="~/assets/icons/mop.png")
          li Pinol
          li Toallitas Desinfectantes
          li Limpiador de Vidrios
          img(src="~/assets/icons/toilet-paper.png")
          li Aromatizante en aerosol

      .item
        h3 ARTÍCULOS DE ASEO PERSONAL
        ul
          li Jabón líquido para manos
          li Toallitas húmedas
          li Toallas femeninas ultra delgadas y con alitas
          img(src="~/assets/icons/soap.png")
          li Pasta dental (suave)
          li Papel Sanitario
          li Crema Corporal
          li Kleenex
      .item
        h3 ARTÍCULOS DE PAPELERIA
        ul
          li Papel Bond Blanco
          li Papel Bond Colores
          li Plumas
          li Lápices
          img(src="~/assets/icons/pencils.png")
          li Lápices de Colores
          li Resistol Blanco
          li Pritt
          li Pinturas Dactilares
          li Acuarelas
          li Catulinas
          li Fommie
          li Pistolas de Silicón
          li Pilas: A, AA, C, D
      
      .item
        h3 DONATIVOS CON CARGO DIRECTO A TARJETA DE CRÉDITO
        p Ponte en contacto con nosotros 
        img(src="~/assets/icons/teamwork.png")
      .item
        h3 VOLUNTARIADO
        p Apoyando directamente con tu tiempo y ayudando directamente en la rehabilitación de los niños y jóvenes. Puedes apoyar también con tus servicios profesionales (Apoyo administrativo, contable, mercadotecnia, diseño, sistemas, etc.).
        img(src="~/assets/icons/volunteer.png")
      .item
        h3 SERVICIO SOCIAL
        p Si estás acabando tu carrera y necesitas realizar tu servicio social, ponte en contacto con nosotros. Tenemos diferentes planes tanto presenciales como por proyectos. Estamos registrados ante varias universidades para la realización de servicio social de su alumnado.
        img(src="~/assets/icons/babysitter.png")

</template>

<script>
  export default {
    name: "Apoyo",

    data() {
      return {
        rezised: 0,
        title: "Asomas | Apoyo",
        description: "Apoyo para Asomas"
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
  #apoyo
    line-height: 35px
    color: #363636
    margin-bottom: 40px
  li
    list-style: none
  hgroup
    text-transform: uppercase
    color: #00CDB3
    line-height: 2.3em
    font-size: 1.4em
  .item
    transition: .3s
    img
      width: 90px

    &:hover 
      transform: scale(1.01) translateY(-5px)
      box-shadow: 0 3px 10px 2px #9c9c9c

  .donativos
    justify-content: center
    grid-gap: 15px
    display: grid
    width: 100%
    grid-template-columns: repeat(auto-fill, 350px)
    h2
      background-color: #FF003C 
      grid-column: 1 / -1
      color: #fff
      padding: 10px
      margin: 10px 0
    h3
      background-color: #FFA500
      color: #fff

    .efectivo
      grid-column: 1 / -1

</style>

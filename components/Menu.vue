<template lang="pug">
  .menu
    nav
      .menu-responsive(@click="toggle")
        p Menu
      ul(:class="{ visible: toggable }")
        li.centrar
          router-link.centrar( to="/") Inicio
        li.centrar
          router-link.enlace.centrar(to="/programas") Programas
        li.centrar
          router-link.centrar( to="/logros") Logros
        li.centrar
          router-link.centrar( to="/calendario") Calendario
        li.centrar
          router-link.centrar( to="/informe") Informe
        li.centrar
          router-link.centrar( to="/apoyo") Apoyo
        li.centrar
          a.centrar(href='#') Beneficiarios 
        li.centrar
          a.centrar(href='#') Galeria
        li.centrar
          a.centrar( @click="onScroll('contacto')" @click.self.prevent, href='#contacto') Contacto


</template>

<script>
  export default {
    name: "myMenu",
    data(){
      return {
        toggable: false
      }
    },
    methods: {
      onScroll(objetivo){
        const $objetivo = document.getElementById(objetivo)
        $objetivo.scrollIntoView({
          behavior: "smooth",
          block: "end"
        })
      },
      toggle(){
        console.log(this.toggable)
        this.toggable ? this.toggable = false : this.toggable = true
      }
    }
  }
</script>

<style lang="sass" scoped>

.menu
  position: fixed
  background-color: rgba(255, 255, 255, 0.9)
  width: 100%
  display: flex
  top: 0
  height: 50px
  font-weight: 600
  z-index: 10
  nav
    width: 100%
    height: 50px
  ul
    height: 50px
    width: 100%
    display: grid
    grid-template-columns: repeat(9, minmax(max-content, 1fr))
    @media screen and (max-width: 770px)
      display: grid
      position: fixed
      height: calc(100vh - 50px)
      width: 100%
      top: 50px 
      left: 0 
      right: 0 
      bottom: 0 
      grid-template-columns: 1fr 
      background-color: rgba(100,200,200,.9) 
      z-index: 100 
      transform: translateX(-100%)
      transition: .5s
  a
    width: 100%
    color: rgba(2, 109, 95, 0.9)
    text-decoration: none
    height: 100%
  li
    transition: .3s
    &:hover
      box-shadow: inset 0px -5px #00CDB3
  

  .menu-responsive
    display: none
    background-color: #FF003C
    color: #fff
    height: 100%
    p
      margin: auto
    @media screen and (max-width: 770px)
      display: grid
      text-align: center
      vertical-align: middle
    
  
  .visible
    // transition: .5s
    transform: translateX(0)

</style>

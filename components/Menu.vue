<template lang="pug">
  .menu
    nav
      .menu-responsive(@click="toggle")
        p Menu
      ul(:class="{ visible: toggable }", @click="salir")
        li.centrar(:class="{ 'is-active': 'index' === actived }")
          router-link.centrar( to="/") Inicio
        li.centrar(:class="{ 'is-active': 'programas' === actived }")
          router-link.enlace.centrar(to="/programas") Programas
        li.centrar(:class="{ 'is-active': 'logros' === actived }")
          router-link.centrar( to="/logros") Logros
        li.centrar(:class="{ 'is-active': 'calendario' === actived }")
          router-link.centrar( to="/calendario") Calendario
        li.centrar(:class="{ 'is-active': 'informe' === actived }")
          router-link.centrar( to="/informe") Informe
        li.centrar(:class="{ 'is-active': 'apoyo' === actived }")
          router-link.centrar( to="/apoyo") Apoyo
        li.centrar(:class="{ 'is-active': 'beneficiarios' === actived }")
          router-link.centrar( to="/beneficiarios") Beneficiarios 
        li.centrar(:class="{ 'is-active': 'galeria' === actived }")
          router-link.centrar( to="/galeria") Galeria 
        li.centrar
          a.centrar( @click="onScroll('contacto')", @click.self.prevent, href='#contacto') Contacto


</template>

<script>
  export default {
    name: "myMenu",
    data(){
      return {
        toggable: false,
        actived: ''
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
        this.toggable ? this.toggable = false : this.toggable = true
      },
      salir(){
        this.toggable = false
      }
    },
    created () {
      this.$bus.$on('menu', (data) => this.actived = data )
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

  .is-active
    box-shadow: inset 0px -5px #00CDB3


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
      height: calc(100vh-50px)
      top: 50px 
      left: 0 
      right: 0 
      bottom: 0 
      grid-template-columns: 1fr 
      z-index: 100 
      transform: translateX(-100%)
      transition: 1s
      z-index: 20
  a
    color: rgba(2, 109, 95, 0.9)    
    width: 100%
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
    display: grid
    transition: .5s
    background-color: rgba(0, 0, 0, .7)
    transform: translateX(0)
    a
      color: #fff
    &:active
      background-color: rgba(2, 109, 95, 0.9)
</style>

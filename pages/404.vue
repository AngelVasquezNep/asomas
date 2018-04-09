<template lang="pug">
  .container.centrar
    h1(v-if="error.statusCode === 404") Lo sentimos, no hallamos la ruta "asomas.org.mx{{ error.path }}"
    h1(v-else) Ocurrió un error inesperado, si el problema persiste, reportelo a nuestro correo, por favor. Saludos
    .btn
      nuxt-link(to="/") Regresar a la página principal
    img(src='~/assets/logo.png', alt='Asomas')
    
  </div>
</template>

<script>
export default {
  props: ['error'],
  mounted() {
    console.log(this.error)
  }
}
</script>

<style lang="sass" scoped>
h1
  margin: 30px
  color: #FF003C

.btn
  margin: 25px auto
  width: 90%
  border: 3px solid #FF003C
  border-radius: 10px
  transition: .5s
  outline: none
  a
    padding: 10px
    text-decoration: none
    display: block
    transition: .5s
    font-weight: bold
    color: #fff
    color: #FF003C
    font-size: 1.3em
    width: 100%
    height: 100%
  &:hover
    background-color: #FF003C
    a
      color: #fff
  &:active
    transform: scale(0.98)
</style>

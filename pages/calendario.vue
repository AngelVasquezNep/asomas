<template lang="pug">
  #calendario.centrar
    hgroup
      h2 Siempre estamos para ti 
      h3 Recuerda que si tienes alguna duda, nuestros teléfonos están abajo
    img(src="~/assets/calendario.png")
</template>

<script>
  export default {
    name: "Calendario"
  }
</script>

<style lang="sass" scoped>
  #calendario
    color: #515151
    img
      width: 100%
</style>

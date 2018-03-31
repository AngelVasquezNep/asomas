<template>
  <v-touch @swipeleft="swipeleft" @swiperight="swiperight">
    <myMenu />
    <nuxt class="mynuxt"/>
    <myContacto/>
  </v-touch>
</template>

<script>
  import myMenu from '~/components/Menu.vue'
  import myContacto from '~/components/Contacto.vue'

  export default {
    components: { myMenu, myContacto },
    methods:{
      swipeleft() {
        this.$bus.$emit('izDer', "De derecha a izquierda")
      },
      swiperight() {
        this.$bus.$emit('derIz', "De izquierda a derecha")
      }
    }
  }
</script>

<style lang="sass">

*
  margin: 0
  padding: 0
  font-family: 'Montserrat', sans-serif

.mynuxt
  margin-top: 50px  

.centrar
  display: flex
  justify-content: center
  align-items: center
  text-align: center
  flex-direction: column


</style>

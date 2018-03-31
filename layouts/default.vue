<template>
<div>
    <myMenu />
    <nuxt class="mynuxt"/>
    <myContacto/>
</div>
</template>

<script>
  import myMenu from '~/components/Menu.vue'
  import myContacto from '~/components/Contacto.vue'

  export default {
    components: { myMenu, myContacto }
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

<template lang="pug">
  #beneficiarios.centrar
    h1 Beneficiarios
    .subtitulo
      h2 Directos
    ul
      li > En los 15 años que lleva ASOMAS se han atendido directamente a más de 400 niños con sus familias.
      li > En el ciclo escolar 2015-2016, atendemos a 28 niños bajo el Programa Básico.
      li > En este ciclo escolar se atienden tres alumnos en el Programa en Casa, uno del Estado de Coahuila y dos del Estado de Hidalgo.
      li > Todos los padres de familia son capacitados por lo menos una vez mes con temas selectos que apoyan el desarrollo de sus hijos. De igual modo, en las clases públicas se enseña a los padres que asisten a las instalaciones la manera de realizar la rehabilitación de sus hijos en casa.
      li > Actualmente se capacitan en línea un aproximado de 125 personas entre docentes y padres de familia mexicanos.
    .subtitulo
      h2 Indirectos
    ul
      li > ASOMAS capacita continuamente a estudiantes y profesionistas en educación especial y profesionistas por medio del programa de Capacitación, en el que se imparten cursos en nuestras instalaciones o en otras instituciones afines.
      li > De la misma forma se han capacitado a futuros docentes de las diferentes especialidades (Intelectual, visual. Motor, problemas de aprendizaje, audición y lenguaje) a nivel nacional (Baja California Sur, Tabasco, Veracruz, y Cuidad de México…) Quienes a su vez replican el modelo de atención de ASOMAS que favorece el desarrollo integral en personas con sordoceguera y/o multidiscapacidad a su cargo.
      li > El impacto que el Programa a Padres tiene se extiende por lo menos a 4.5 familiares o personas allegadas por niño atendido, ya que forman parte del cuidado, atención y/o rehabilitación de los niños discapacitados.
</template>

<script>
  export default {
    name:"Beneficiarios",

    data() {
      return {
        rezised: 0,
        title: "Asomas | Beneficiarios",
        description: "Beneficiarios de Asomas"
      }
    },
    head () {
      return {
        title: this.title,
        meta: [
          { hid: 'description', name: 'description', content: this.description }
        ]
      }
    },

    mounted () {
      this.$bus.$emit('menu', 'beneficiarios')
    }

  }
</script>

<style lang="sass" scoped>
#beneficiarios
  user-select: none
  display: grid
  line-height: 30px
  margin-bottom: 30px
  grid-template-columns: minmax(100px, 300px) 1fr
  grid-gap: 40px
  animation: apper .5s
  will-change: opacity
  @keyframes apper 
    0%
      opacity: 0
  @media screen and (max-width: 768px)
    grid-template-columns: 1fr
    .subtitulo
      padding: 10px 0

  ul
    list-style: none
  li
    user-select: none
    &:hover
      background-color: #FF003C
      color: #fff
      cursor: pointer
  h1
    background-color: #00CDB3
    color: #fff
    width: 100%
    padding: 40px 0
    grid-column: 1 / -1
    margin-top: 10px
  .subtitulo
    color: #fff
    background-color: #FFA500
    height: 100%
    display: grid
    &:nth-of-type(2)
      background-color: #FF003C
    h2
      font-size: 2em
      margin: auto
</style>

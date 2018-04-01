<template lang="pug">
  #programas.programas.centrar
    h1 PROGRAMAS Y SERVICIOS

    p En ASOMAS sabemos que cada niño o joven con retos múltiples necesita una atención especial y personalizada. Cada grado y agudeza de discapacidad es diferente, y cada situación familiar única, afectando así su desarrollo. De ahí que se han diseñado diferentes programas que tienen como finalidad crear las oportunidades de un entorno adecuado para los alumnos y sus familias con el fin de proporcionarles una mejor calidad de vida.
    
    ol.programas-lista
      li.lista
        h2 PROGRAMA BÁSICO
        p Este servicio ofrece educación, estimulación y rehabilitación a niños y jóvenes, en un horario de lunes a viernes de 9:00 am a 1:00 pm y de lunes a viernes de 3:00 a 6:00 pm.
        img(v-lazy="require('~/assets/img1.jpg')")
      li.lista
        h2 PROGRAMA EN CASA
        p El Programa en Casa ofrece servicios básicos de educación, estimulación y rehabilitación a niños y jóvenes pero que, por causas del grado de su discapacidad, o por contar con escasos recursos no pueden desplazarse a nuestras instalaciones. Nuestro personal diseña programas individuales y capacita a los padres de familia para que la rehabilitación e inclusión sea realizada en sus casas. Los padres de familia junto con los alumnos asisten cada quince días a las instalaciones de ASOMAS para ser evaluados y ver que su evolución sea la esperada. En estas visitas se valora y modifica el programa y se dan las recomendaciones pertinentes para continuar con la rehabilitación.
        img(v-lazy="require('~/assets/img2.jpg')")

      li.lista
        h2 PROGRAMA A PADRES
        p El progreso y la evolución de los alumnos depende en gran medida del apoyo que sus padres y familiares les brinden es por eso que ASOMAS apoya a los padres de familia, mediante asesoría y capacitación periódica a través de talleres, cursos y grupos de autoayuda.
        img(v-lazy="require('~/assets/img3.jpg')")
  
      li.lista
        h2 PROGRAMA DE CAPACITACIÓN
        p   ASOMAS capacita a docentes y centros educativos en lo referente a sordoceguera y multidiscapacidad. El objetivo primordial es multiplicar el modelo de atención llevado en la institución. Como apoyo a las capacitaciones se coordinan visitas a ASOMAS para que las instituciones y/o docentes resuelvan dudas e inquietudes directamente en la institución.
        img(v-lazy="require('~/assets/img4.jpg')")

      li.lista
        h2 PROGRAMA INTEGRAL DE NUTRICIÓN
        p En ASOMAS estamos conscientes de la importancia que tiene la alimentación como parte fundamental en el crecimiento y desarrollo de los niños, así como de su estado general de salud. Es por eso que contamos con el apoyo de una Nutrióloga, que da recomendaciones sobre hábitos alimenticios y en caso de ser necesario, desarrolla un plan de nutrición adecuado a las necesidades de los alumnos.
        img(v-lazy="require('~/assets/img5.jpg')")
      li.lista
        h2 PROGRAMA INTEGRAL DE PSICOLOGÍA
        p Centrado en orientar y brindar atención a niños y jóvenes con sordoceguera y/o discapacidad múltiple, padres de familia y maestras, con el objetivo de brindar las herramientas necesarias que favorezcan el desarrollo psicosocial del individuo.
        img(v-lazy="require('~/assets/img1.jpg')")
      li.lista
        h2 TRANSICIÓN A LA VIDA ADULTA
        p El objetivo principal es desarrollar la autonomía e independencia de nuestros alumnos en esta etapa y orientar a los padres de familia sobre cómo lograr que esta etapa sea llevada de la mejor manera. Al mismo tiempo se desarrollan actividades pre-laborales para así lograr un cierto grado de independencia a los alumnos en esta etapa.
        img(v-lazy="require('~/assets/img2.jpg')")
      li.lista
        h2 FISIOTERAPIA
        p El objetivo principal del programa de Fisioterapia es potencializar las habilidades motrices, favorecer la independencia y el desarrollo psicomotor de los alumnos. Se realizan programas individuales de acuerdo a las diferentes necesidades de rehabilitación física de cada uno de ellos.
        img(v-lazy="require('~/assets/img3.jpg')")
      li.lista
        h2 TRABAJO SOCIAL
        p El objetivo principal es el conocimiento de la familia y el entorno social de cada alumno para optimizar los recursos a su disposición y favorecer la integración a la familia y a su comunidad.
        img(v-lazy="require('~/assets/img4.jpg')")

</template>

<script>

export default {
    name: "Programas",
    data() {
      return {
        title: "Asomas | Programas y servicios",
        description: "Programas y servicios de Asomas"
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

    mounted() {
      this.$bus.$emit('menu', 'programas')
    }

  }
</script>

<style lang="sass" scoped>
  .programas
    font-size: 1.2em
    line-height: 45px
    font-family: 'Montserrat', sans-serif
    h1 
      margin: 30px 0
    .programas-lista
      list-style: none
      padding: 0 3em 
      line-height: 35px
      @media screen and (max-width: 600px)
        padding: 10px
      .lista
        display: grid
        margin: 10px 0
        align-items: center
        grid-template-columns: 1fr 1fr
        @media screen and (max-width: 768px)
          &:nth-of-type(2n)
          grid-template-areas: "titulo" "img" "descripcion" !important
          grid-template-columns: 1fr !important

      
        

        h2
          padding: 10px
          color: #fff
          grid-area: titulo 
        p
          grid-area: descripcion
          padding: 10px
        img
          grid-area: img
          width: 100%

        &:nth-of-type(2n)
          grid-template-areas: "titulo titulo" "img descripcion"
          grid-template-columns: 45% 1fr
          h2 
            background-color: #FFA500
        
        &:nth-of-type(2n+1)
          grid-template-areas: "titulo titulo" "descripcion img"
          grid-template-columns: 1fr 45%
          h2 
            background-color: #00CDB3

        &:nth-of-type(3n)
          h2 
            background-color: #FF003C
          
</style>

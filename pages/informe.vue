<template lang="pug">
  #informe.centrar
    hgroup
      H1 INFORME
      p Introducción En 2016 la Asociación Mexicana Anne Sullivan IAP (ASOMAS) cumple 15 años de brindar atención a niños y jóvenes con sordoceguera y discapacidad múltiple. ASOMAS es una Institución de Asistencia Privada sin fines de lucro que tiene la misión de fomentar el desarrollo integral de personas sordociegas y/o con discapacidad múltiple con el fin favorecer su autonomía e integración a la familia, a la escuela y a la sociedad.

    .informe-container.centrar
      .introduccion
        h2 Introducción
        
        p En 2016 la Asociación Mexicana Anne Sullivan IAP (ASOMAS) cumple 15 años de brindar atención a niños y jóvenes con sordoceguera y discapacidad múltiple. ASOMAS es una Institución de Asistencia Privada sin fines de lucro que tiene la misión de fomentar el desarrollo integral de personas sordociegas y/o con discapacidad múltiple con el fin de lograr una inclusión a nivel familiar, social, escolar y laboral.
        p El modelo de atención que ASOMAS brinda a sus beneficiarios proviene del modelo Perkins Internacional, una institución líder a nivel mundial con presencia en más de 65 países. En México ASOMAS es una de las pocas instituciones en brindar éste modelo de atención.

      .equipo.centrar

        h2 Quienes lo conforman 
        p Con el paso del tiempo nuestra Asamblea y Patronato ha sido renovando, y en 2016 se integran nuevas personas, que con su experiencia y compromiso han logrado dar a Asomas un nuevo giro.

        .tabla
          h2 ASAMBLEA DE ASOCIADOS
          p María del Carmen Galíndez González
          p Fundadora
          p Rosa María Mendiburu Galíndez
          p Asociado
          p Francisco Javier Mendiburu Galíndez
          p Asociado
          p María Nieves Mendiburu Galíndez
          p Asociado
          h2 PATRONATO
          p María Nieves Mendiburu Galíndez
          p Presidente
          p Guadalupe Galíndez González
          p Tesorero
          p Molly Felker King
          p Secretario
          p Lourdes Mendiburu Cenoz
          p Vocal
          p Ma. de los Ángeles Cano García
          p Vocal
          p Rosa María Nadal Sánchez
          p Vocal
          h2 PERSONAL DOCENTE Y ADMINISTRATIVO
          p Yessica Herrera Gutiérrez
          p Coordinadora Académica
          p Rocio Luna Ramírez
          p Recaudación de Fondos
          p Denys Herrera Torres
          p Asistente de Patronato
          p Carolina Concepción Ramírez Godoy
          p Trabajo Social
          p Juana María Velazco Ovando
          p Titular de Grupo
          p Amelia Cortez Urban
          p Titular de Grupo
          p Verónica Reyes Galaviz
          p Titular de Grupo
          p Ivonne González Hernández
          p Titular de Grupo
          p Jaqueline Gómez Trujillo
          p Titular de Grupo
          p Damina Mariana Martínez
          p Titular de Grupo
          p Claren Sánchez Salvador
          p Auxiliar de Grupo
          p Felicia Roa Jasso
          p Auxiliar de Grupo
          p Erika Stephanie Bernal
          p Terapeuta Físico
          p Natalia Nadal Rosas
          p Psicóloga
          p Rosalinda Elizalde Toledo
          p Logoterapeuta
          p Virginia Guzmán Sánchez
          p Intendencia
          p Daniel Omar Guzmán
          p Mensajero
          p Isabel Galíndez Felker
          p Directora General

      .organigrama-content
        h2 Organigrama
        .organigrama(v-show="rezised>=960")
            ul
              li
                a(href='#') Asamblea General de Asociados
                ul
                  li
                    a(href='#') Patronato
                    ul
                      li
                        a(href='#') Dirección General
                    
                        ul
                          li
                            a(href='#') Coordinación de Procuración de fontos
                          li
                            a(href='#') Coordinación Academica

                            ul
                              li
                                a(href='#') Terapia fisica
                              li
                                a(href='#') Especialistas
                              li
                                a(href='#') Trabajo Social
                              li
                                a(href='#') Psicólogia
                          li
                            a(href='#') Asistente
        .organigrama-img(v-show="rezised<960")
          figure
            img(v-lazy="require('~/assets/organigrama.png')")

      
      .impactoSocial
        h2 IMPACTO SOCIAL
        ul
          li Beneficiarios Directos: 33 niños.
          li Beneficiarios Indirectos: 132
          li Capacitaciones: 366 docentes y futuros docentes que beneficiarían de forma directa a aproximadamente a 2,928 alumnos. (Población con sordoceguera y/o multidiscapacidad).
          li Estados Impactos: Estado de México, Ciudad de México, Tlaxcala, Veracruz, Coahuila y Guanajuato.
          li Visitas Institucionales: Universidad IberoAmericana, UNAM, Montessori Lomas, Normal de Especialización de Tlaxcala, Universidad Pedagógica de la Ciudad de México, CAM Tlaxcala, Normal Veracruzana, Universidad de Psicología, Perkins International.
      .vinculacionSocial
        h2 VINCULACIÓN SOCIAL
        ul
          li Uno de los objetivos primordiales de Asomas es fomentar la inclusión tanto laborar como social de nuestros alumnos para lograr un mayor impacto tanto en la formación integral de nuestra población como sensibilizar a la población en general sobre la discapacidad . Durante 2016 logramos establecer la vinculación con diferentes empresas:
          li Hotel Hilton: Empaquetado de producto, prácticas laborales, taller de elaborado de toallas y participación en bazares.
          li Apoyo Económico: Empaquetado de producto, prácticas laborales, taller de elaborado de toallas y participación en bazares.
          li Fundación Telefónica: Visita a las instalaciones de Asomas, Taller para entender la sordoceguera y multidiscapacidad, elaboración de panales sensoriales para uso de los alumnos.
          li Dow: Venta de producto empaquetado por alumnos de Asomas.
          li Inclusión Laboral: Uno de nuestros alumnos con sordoceguera y multidiscapacidad, realiza practicas formales, en una cocina económica .
          li Experiencias Sociales: Dependiendo de la edad, algunos alumnos junto con sus maestros realizan experiencias sociales y recreativas, que consisten en la visita a diferentes lugares dentro de la comunidad ( Salón de belleza, cafetería, restaurantes, tiendas, centros comerciales, visitas al cine, museos, acuario, plantas industriales, parques). Logrando así tener experiencias de acuerdo a su edad y logrando que la población en general tome conciencia de que las actividades de los niños y jóvenes con sordoceguerea y multidiscapacidad, no están limitadas.

</template>

<script>
  export default {
    name:"Informe",
    data(){
      return {
        rezised: 0,
      }
    },
    mounted: function () {
      window.addEventListener('resize', (event)=>{
        this.resise()
      })
    },
    methods: {
      resise(){
        this.rezised = window.innerWidth
      }
    }

  }
</script>

<style lang="sass" scoped>

#informe
  margin-bottom: 50px
  line-height: 35px
  color: #1f1f1f
  h1
    color: #fff
    background-color: #00CDB3
    padding: 30px 0
    margin: 20px
    font-size: 3em
    position: relative
    img
      position: absolute
      width: 40px
      padding: 10px
      top: 17px
  li
    list-style: none

.equipo
  h2
    margin: 20px 0
    width: 100%
    padding: 10px 0
    background-color: #FFA500
    color: #fff

.tabla > *
  // box-shadow: 0 0 0px 1px #FF003C
.tabla
  display: grid
  justify-content: center
  grid-template-columns: 1fr auto
  align-items: none
  width: 70%
  @media screen and (max-width: 768px)
    width: 95%
  h2
    background-color: #FF003C
    color: #fff
    grid-column: 1 / -1
    padding: 10px 0
  p 
    padding: 3px 0
  @media screen and (max-width: 544px)
    grid-template-columns: 1fr
    p
      &:nth-of-type(2n+1)
        margin-top: 15px
        font-size: 1.1em

      &:nth-of-type(2n)
        color: #FF003C
        padding: 0
        line-height: 5px
        font-size: .9em
.organigrama-content
  padding: 20px 0
  h2
    padding: 10px
    margin: 10px 0
    background-color: #FFA500
    color: #fff
  .organigrama-img
    img
      width: 100%
  .organigrama * 
    margin: 0px
    padding: 10px
  

  .organigrama ul 
    padding-top: 20px
    position: relative
  

  .organigrama li 
    float: left
    text-align: center
    list-style-type: none
    padding: 20px 5px 0px 5px
    position: relative
  

  .organigrama li::before, .organigrama li::after 
    content: ''
    position: absolute
    top: 0px
    right: 50%
    border-top: 2px solid #00CDB3
    width: 50%
    height: 20px
  

  .organigrama li::after
    right: auto
    left: 50%
    border-left: 2px solid #00CDB3
  

  .organigrama li:only-child::before, .organigrama li:only-child::after 
    display: none
  

  .organigrama li:only-child 
    padding-top: 0
  

  .organigrama li:first-child::before, .organigrama li:last-child::after
    border: 0 none
  

  .organigrama li:last-child::before
    border-right: 2px solid #00CDB3
    border-radius: 0 5px 0 0
  

  .organigrama li:first-child::after
    border-radius: 5px 0 0 0
  

  .organigrama ul ul::before 
    content: ''
    position: absolute
    top: 0
    left: 50%
    border-left: 2px solid #00CDB3
    width: 0
    height: 20px
  

  .organigrama li a 
    border: 2px solid #00CDB3
    padding: 1em 0.75em
    text-decoration: none
    color: #353535
    font-size: 0.85em
    display: inline-block
    border-radius: 5px
    transition: all .2s
  

  .organigrama li a:hover 
    border: 1px solid #fff
    color: #fff
    background-color: #00CDB3
    display: inline-block
  


.impactoSocial
  padding: 20px 0
  h2
    padding: 10px
    margin: 10px 0
    background-color: #FFA500
    color: #fff

.vinculacionSocial
  padding: 20px 0
  h2
    margin: 10px 0
    padding: 10px
    background-color: #FFA500
    color: #fff

</style>

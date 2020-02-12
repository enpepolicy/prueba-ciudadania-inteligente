<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" md="9">
        <v-card class="pa-5">
          <v-card-title class="display-2">
            Buen dia chicxs,
          </v-card-title>
          <v-card-text class="title">
            <p>Mi nombre es <strong>  Enrique Peña</strong>, soy politologo y desarrollador colombiano, vivo y trabajo en CDMX. Son pocas las veces que veo una oferta laboral y digo "esa es para mi", me paso con ustedes 😅. Espero que mi prueba sea de su agrado....</p>
            <v-divider class="py-3" />
            <p class="subtitle-1 ">
              Uds. solicitaban  un desarrollo que pudiese cumplir las funciones de <strong>Jekyll</strong>, por lo cual opte por una tecnologia de pre-renderizado llamada Nuxt.js y su comando <strong>nuxt generate</strong>, a partir de Node.js me es posible renderizar desde el back-end y layouts un sitio web completamente estatico y SEO-friendly.
            </p>
            <p class="subtitle-1 ">
              Igualmente, fue solicitada una alternativa que cumpliera la función de una coleccion de Jekyll, para lo cual opte por nutrir el sistema a partir de un archivo JSON con la información de las elecciones con el siguiente esquema:
            </p>
            <v-img
              :src="require('@/assets/code.png')"
            />
            <a class="subtitle-1 text-end" href="https://github.com/enpepolicy/prueba-ciudadania-inteligente/blob/master/static/elections.js" target="_blank"> Json completo acá</a>
            <p class="body-2 text-right pt-6">
              Como vi que el diseño no seria evaluado, no le meti mucho. <br>No obstante, me siento comodo en el front tambien. <br>(Disculpen los typos y tildes, no les hice revisión de redacción rigurosa.)
            </p>
          </v-card-text>
          <v-card-actions>
            <v-row justify="center">
              <v-btn
                x-large
                color="primary"
                nuxt
                to="/elections"
              >
                Ver Prueba
              </v-btn>
            </v-row>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  components: {
  }
}
</script>
<style lang="scss">
code{
  border-radius: 0;
  background-color: white;
  box-shadow: none;
  -webkit-box-shadow: none;
  margin: 1em
}
.caption-2{
  font-size: 0.8em
}

</style>

<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-container>
        <v-row justify="center" align="center">
          <h1 class="text-center">
            Prueba Enrique Peña ✊
          </h1>
          <v-spacer />
          <v-btn
            href="https://github.com/enpepolicy/prueba-ciudadania-inteligente"
            target="_blank"
            class="mx-2"
            rounded
            color="blue"
          >
            <span class="white--text">
              Repo
            </span>
          </v-btn>
          <v-btn
            class="mx-2"
            to="/"
            rounded
            color="orange"
          >
            <span class="white--text">
              Leanme
            </span>
          </v-btn>
        </v-row>
      </v-container>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

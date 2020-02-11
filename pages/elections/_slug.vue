<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="5">
        <v-card
          class="my-4 mx-2 pa-4 "
        >
          <v-row justify="center">
            <v-img
              max-height="8em"
              contain
              eager
              :src="election.flagUrl"
            />
          </v-row>
          <v-card-subtitle class="pt-5 pb-1 font-weight-black white--text">
            El dia <span class="orange--text">{{ election.date }} de 2020</span>  seran llevadas a cabo las elecciones a nivel {{ election.level }} de <span class="orange--text"> {{ election.country }}</span>. Estas elecciones seran {{ election.type }} y representan una jornada más en la historia democratica latinoamericana.
          </v-card-subtitle>

          <v-card-actions class="pt-3 pb-0">
            <v-row justify="center">
              <v-btn
                to="/elections"
                class="mx-2"
                rounded
                color="white"
              >
                <span class="black--text">
                  Ir atras
                </span>
              </v-btn>
              <v-btn
                :href="election.moreInfo"
                target="_blank"
                class="mx-2"
                rounded
                color="orange"
              >
                <span class="white--text">
                  Ver fuente externa
                </span>
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
  data: () => ({
    election: {}
  }),
  created () {
    this.election = this.$store.state.elections.find(x => x.slug === this.$route.params.slug)
    // eslint-disable-next-line
    console.log(this.election)
  }
}
</script>

<style>

</style>

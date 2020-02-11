<template>
  <v-container>
    <v-row>
      <v-col v-for="election in $store.state.elections" :key="election.slug" lg="3" sm="4" cols="6">
        <v-card
          hover
          :to="`elections/${election.slug}`"
          color="#4f4f4f"
          class="my-4 mx-2 pa-4"
          max-width="400"
        >
          <v-row justify="center">
            <v-avatar size="92">
              <v-img
                contain
                eager
                :src="election.flagUrl"
              />
            </v-avatar>
          </v-row>
          <v-card-subtitle class="pt-0 pb-1 font-weight-black text-center white--text">
            {{ election.country }}
          </v-card-subtitle>
          <v-card-text class="orange--text pa-0 py-1">
            <div class="text-center">
              Elecciones {{ election.type }}
            </div>
            <div class="text-center">
              Nivel {{ election.level }}
            </div>
            <div class="text-center white--text">
              {{ election.date }}
            </div>
          </v-card-text>

          <v-card-actions class="pt-3 pb-0">
            <v-btn
              block
              rounded
              color="white"
            >
              <span class="black--text">
                Ver más
              </span>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

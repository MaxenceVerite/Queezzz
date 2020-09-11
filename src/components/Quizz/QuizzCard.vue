<template>
  <v-hover :value="24">
    <v-card
      slot-scope="{ hover }"
      :class="`elevation-${hover ? 12 : 2}`"
      :loading="loading"
      class="mx-auto my-12"
      max-width="374"
    >
      <v-img height="250" src="https://cdn.vuetifyjs.com/images/cards/cooking.png"></v-img>

      <v-card-title>Cuisine Britannique</v-card-title>

      <v-card-text>
        <v-row align="center" class="mx-0">
          <v-rating :value="3.8" color="amber" dense half-increments readonly size="14"></v-rating>

          <div class="grey--text ml-4">4.5 (1207)</div>
        </v-row>

        <div class="my-4 subtitle-1">
          <span>Facile</span>
        </div>

        <div>Alimentation anglaise, du petit dejeuné au souper.</div>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-title>Disponibilité</v-card-title>

      <v-card-text>
        <v-chip-group>
          <v-chip>
            <v-icon color="green">mdi-clipboard-play-outline</v-icon>07/06/2020
          </v-chip>
          <v-chip>
            <v-icon color="red">mdi-calendar-remove-outline</v-icon>13/07/2020
          </v-chip>
        </v-chip-group>
      </v-card-text>

      <v-card-actions>
        <v-btn color="amber darken-3 lighten-2" text @click="$router.push('quizz')">Jouer</v-btn>
      </v-card-actions>
    </v-card>
  </v-hover>
</template>
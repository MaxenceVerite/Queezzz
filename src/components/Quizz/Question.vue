<template>
  <v-card class="question d-inline-block mx-auto" width="40%">
    <span v-if="choixUnique">
      <v-card-title>
        <v-row>
          <v-col>
            <v-img class="rounded" height="40px" width="40px" src="@/assets/icons/hexagon.png"></v-img>
          </v-col>
          <v-col>Ceci est l'intitulé de la question ?</v-col>
        </v-row>
      </v-card-title>
      <v-container>
        <v-radio-group v-model="radios" :mandatory="false">
          <v-radio label="Réponse 1" value="radio-1"></v-radio>
          <v-radio label="Réponse 2" value="radio-2"></v-radio>
          <v-radio label="Réponse 3" value="radio-3"></v-radio>
          <v-radio label="Réponse 4" value="radio-4"></v-radio>
        </v-radio-group>
      </v-container>
    </span>
    <span v-else>
      <v-card-title>
        <v-container>
          <v-row>
            <v-col>
              <v-img
                class="rounded"
                height="40px"
                width="40px"
                src="@/assets/icons/tri-hexagon.png"
              ></v-img>
            </v-col>
            <v-col>Intitulé</v-col>
          </v-row>
        </v-container>
      </v-card-title>
      <v-container>
        <v-checkbox v-model="selected" label="Réponse 1" value="rep1"></v-checkbox>
        <v-checkbox v-model="selected" label="Réponse 2" value="rep2"></v-checkbox>
        <v-checkbox v-model="selected" label="Réponse 3" value="rep3"></v-checkbox>
        <v-checkbox v-model="selected" label="Réponse 4" value="rep4"></v-checkbox>
      </v-container>
    </span>
  </v-card>
</template>
<script>
export default {
  props: {
    choixUnique: Boolean
  }
};
</script>
<style>
.question {
  border-bottom: black solid 1px;
  margin-bottom: 5px;
}
</style>
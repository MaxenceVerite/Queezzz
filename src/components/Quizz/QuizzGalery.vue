<template>
  <v-container fluid>
    <v-row>
      <v-col v-for="n in 20" :key="n" cols="6" sm="4">
        <span v-if="n % 2 === 0">
          <QuizzCard :choixUnique="false" />
        </span>
        <span v-else>
          <QuizzCard :choixUnique="true" />
        </span>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import QuizzCard from "@/components/Quizz/QuizzCard";

export default {
  name: "QuizzGalery",

  components: { QuizzCard }
};
</script>
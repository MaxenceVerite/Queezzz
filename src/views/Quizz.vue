<template>
  <v-container>
    <v-row v-for="n in 10" :key="n">
      <Question />
    </v-row>
  </v-container>
</template>
<script>
import Question from "@/components/Quizz/Question";

export default {
  components: {
    Question
  }
};
</script>
<style>
</style>
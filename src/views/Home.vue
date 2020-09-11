<template>
  <div class="home">
    <QuizzGalery />
  </div>
</template>

<script>
// @ is an alias to /src
import QuizzGalery from "@/components/Quizz/QuizzGalery";
export default {
  name: "Home",
  components: { QuizzGalery }
};
</script>

<template>
  <div class="home">
    <Question />
  </div>
</template>

<script>
// @ is an alias to /src
import Question from "@/components/Question.vue";

export default {
  name: "Home",
  components: {
    Question
  }
};
</script>

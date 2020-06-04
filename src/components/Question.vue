/* eslint-disable vue/valid-v-for */
<template>
  <div class="wrapper">
    <div v-for="q in questionAndAnswers" :key="q.id" class="qa-wrapper">
      <h1 class="question">{{ q.question }}</h1>
      <ol>
        <Answer v-for="a in q.answers" v-bind:answer="a" v-bind:key="a" />
      </ol>
    </div>
  </div>
</template>

<script>
import Answer from "@/components/Answer.vue";
import data from "@/assets/qa.json";

export default {
  name: "Question",
  props: {
    msg: String
  },
  components: {
    Answer
  },
  computed: {
    questionAndAnswers() {
      return data.questions;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.qa-wrapper {
  min-height: 100vh;
}
.question {
  display: inline-block;
  font-family: Visitor1, sans-serif;
  padding: 20px 40px;
  background-color: #060606;
  color: #f5df22;
  font-size: 42px;
  max-width: 75vw;
  border: 4px inset #5858e8;
  border-radius: 5px;
}
h3 {
  margin: 40px 0 0;
}
ol {
  max-width: 75vw;
  padding: 0;
  margin: 0 auto;
}
</style>

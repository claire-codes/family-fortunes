/* eslint-disable vue/valid-v-for */
<template>
  <div class="wrapper">
    <div v-for="q in questionAndAnswers" :key="q.id">
      <h1>{{ q.question }}</h1>
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
.answer {
  // display: none;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

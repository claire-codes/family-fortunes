<template>
  <div class="wrapper">
    <h1>Name a type of red liquid</h1>
    <ol>
      <Answer answer="Blood" />
      <Answer answer="Wine" />
      <Answer answer="Ketchup" />
      <Answer answer="Ink" />
      <Answer answer="Paint" />
    </ol>
  </div>
</template>

<script>
import Answer from "@/components/Answer.vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    Answer,
  },
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

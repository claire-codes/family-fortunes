<template>
  <div class="wrapper">
    <li>
      <span><span class="answer" v-show="isOpen">{{ answer }}</span>
      <button @click="toggle()" type="button">?</button></span>
    </li>
  </div>
</template>

<script>
export default {
  name: "Answer",
  props: {
    answer: String
  },
  data: function() {
    return { isOpen: false };
  },
  methods: {
    toggle: function() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@font-face {
  font-family: 'Visitor1';
  src:  url('../assets/visitor1.woff') format('woff');
}

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
  font-family: 'Visitor1', cursive;
}
a {
  color: #42b983;
}
</style>

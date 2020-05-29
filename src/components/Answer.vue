<template>
  <div class="wrapper">
    <li>
      <span class="answer" v-show="isOpen">{{ answer }}</span>
      <button @click="toggle()" type="button">?</button>
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

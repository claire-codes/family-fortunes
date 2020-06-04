<template>
  <li>
    <div class="wrapper">
      <div class="answer" v-show="isOpen">{{ answer }}</div>
      <div class="button-wrapper">
        <button @click="toggle()" type="button">?</button>
      </div>
    </div>
  </li>
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
  font-family: "Visitor1";
  src: url("../assets/visitor1.woff") format("woff");
}

.wrapper {
  display: flex;
  padding: 10px 10px 10px 20px;
  align-items: center;
}
.button-wrapper {
  flex-grow: 1;
  text-align: right;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 10px 0;
  font-family: "Visitor1", cursive;
  background-color: #060606;
  color: #f5df22;
  font-size: 42px;
  border: 4px inset #5858e8;
  border-radius: 5px;
}
button {
  height: 100%;
  width: 50px;
  border: none;
  font-family: Visitor1, sans-serif;
  font-size: 42px;
  border: 3px solid #f5df22;
  background-color: transparent;
  color: #f5df22;
}
</style>

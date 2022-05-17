<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="wrapper">
      <ChildLeft></ChildLeft>
      <ChildRight></ChildRight>
    </div>
  </div>
</template>

<script>
import ChildLeft from "./modules/ChildLeft.vue";
import ChildRight from "./modules/ChildRight.vue";
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  components: { ChildLeft, ChildRight }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.wrapper{
  display: flex;
}

.ChildLeft{
  background-color: skyblue;
    flex: 1;
}
.wrapper>section{
  border:1px solid black;
  height: 200px;
}
.ChildRight{
  flex: 1;
}
</style>

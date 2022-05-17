<template>
  <section class="ChildRight">
    ChildRight{{number}}
    <RightChild></RightChild>
  </section>
</template>

<script>
import RightChild from "./Child/RightChild.vue";
export default {
  name: "ChildRight",
  data() {
    return {
        number:undefined
    };
  },
  components: { RightChild },
  watch: {},
  mounted() {
    this.$bus.$on("hello", (number) => {
        this.number = number
    });
  },
  beforeDestroy(){
    this.$bus.$off('hello')
  },
  methods: {}
};
</script>

<style></style>

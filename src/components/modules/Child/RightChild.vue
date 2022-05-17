<template>
  <section class="RightChild">RightChild {{ number }}</section>
</template>

<script>
export default {
  name: "RightChild",
  data() {
    return {
      number: undefined
    };
  },
  components: {},
  watch: {},
  mounted() {
    this.$bus.$on("hello", this.handleBusHello);
  },
  beforeDestroy() {
    this.$bus.$off("hello");
  },
  methods: {
    handleBusHello(number) {
      this.number = number+10;
    }
  }
};
</script>

<style></style>

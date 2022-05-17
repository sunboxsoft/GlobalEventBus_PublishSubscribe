<template>
  <section class="ChildLeft">
    ChildLeft <button @click="handleSend">$bus发射</button>
  <LeftChild></LeftChild>
  </section>
</template>

<script>
import LeftChild from './Child/LeftChild.vue';
export default {
  name: "ChildLeft",
  data() {
    return {};
  },
  components: {LeftChild },
  watch: {},
  mounted() {},
  methods: {
    handleSend() {
        this.$bus.$emit('hello',666)
    }
  }
};
</script>

<style></style>

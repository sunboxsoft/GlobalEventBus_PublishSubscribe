<template>
  <section class="LeftChild">
    LeftChild{{msgPubsub}}
    <button @click="handleTestPid">测试pid</button>
  </section>
</template>

<script>
import pubsub from "pubsub-js";
export default {
  name: "LeftChild",
  data() {
    return {
        msgPubsub:undefined
    };
  },
  components: {},
  watch: {},
  mounted() {
    this.pid= pubsub.subscribe('hiFun',this.handlePubsub)
    console.log(this.pid,'this.pid')
  },
  methods: {
      handlePubsub(funName,parameter){
          console.log(funName,parameter,this)
          this.msgPubsub = parameter
      },
      handleTestPid(){
          console.log(this.pid,'handleTestPid(){')
      }
  },
  beforeDestroy(){
      pubsub.unsubscribe(this.pid)
  }
};
</script>

<style></style>

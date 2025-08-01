<template>
  <h1>nextTick API Test</h1>
  <span>count : {{ count }} </span><br />
  <button class="btn_test" @click.once="increment">+1</button>
</template>

<script>
import { nextTick } from "vue";

export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
      nextTick(() => {
        console.log("현재 count는 [" + this.count + "]입니다");
      });
    },
  },
};
</script>

<style>
.btn_test {
  background-color: aquamarine;
}
</style>






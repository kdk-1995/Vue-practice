<template>
    <Child title="무선이어폰" price="129000" @changelength="updatePrice" />
    <Child title="블루투스 이어폰" price="99000" @changelength="updatePrice"/>
    <Child title="스마트워치" price="189000" @changelength="updatePrice"/>

    <h2>총가격 : {{totalPrice}} 원</h2>

</template>

<script>
import Child from './Child.vue';

export default {
  data() {
    return {
      totalPrice : 0
    }
  },
  components: {
    Child
  },
  methods : {
    updatePrice(itemKey,price, quantity){
      this.totalPrice += price * quantity
    }
  }
}
</script>

<style>

</style>
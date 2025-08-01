<template> 
    <Child title="무선이어폰" price="129000"  v-model="quantity1" @changed="updatePrice"/>
    <Child title="블루투스 이어폰" price="99000" v-model="quantity2" @changed="updatePrice"/>
    <Child title="스마트워치" price="189000"  v-model="quantity3"  @changed="updatePrice"/>

    <h2>총가격 : {{totalPrice}} 원</h2>

</template>

<script>
import Child from './Child-model.vue';

export default {
  data() {
    return {
      quantity1: 0,
      quantity2: 0,
      quantity3: 0,
      totalPrice : 0
    }
  },
  components: {
    Child
  },
  methods : {
    updatePrice(price, quantity){
        this.totalPrice = 129000 * this.quantity1 +99000 * this.quantity2 +189000 * this.quantity3;
    }
  }
}
</script>

<style>

</style>
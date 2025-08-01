<template>
    <div>체크된 이름: {{ checkedNames }}</div>
    <input type="checkbox" id="jack" value="젝" v-model="checkedNames">
    <label for="jack">젝</label>

    <input type="checkbox" id="john" value="존" v-model="checkedNames">
    <label for="john">존</label>

    <input type="checkbox" id="mike" value="마이크" v-model="checkedNames">
    <label for="mike">마이크</label>
    
    <Increment/>
</template>

<script>
import Increment from './Increment.vue'

export default {
  components: { Increment },
  data() {
    return {
      checkedNames: []
    }
  }
}
</script>

<style>

</style>
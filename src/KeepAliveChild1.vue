<template>
  <div>
    <h3>성명</h3>
    <input v-model="name" placeholder="이름을 입력하여 주십시오"/>
  </div>
</template>

<script>
export default {
  data(){
    return{
      name :''
    }
  }
}
</script>

<style>

</style>
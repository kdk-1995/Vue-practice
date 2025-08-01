<template>
    <h1 class="title">hello world</h1>
    <span>메세지 : {{msg}}</span>
    <button @click="changeMsg" style="margin-left: 10px; background-color: aquamarine;">변경 버튼</button>
</template>

<script>
export default {
    data(){
        return {
            msg : '반갑습니다 Vue.js'
        }
    },
    methods : {
        changeMsg(){
            this.msg = '변경된 msg 입니다'
        }
    }
}
</script>

<style>

</style>








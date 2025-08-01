<template>
    <div>
        <h3>성별</h3>
        <input v-model="gender" type="radio" value="male"/>
        <label>남자</label>
        <input v-model="gender" type="radio" value="female"/>
        <label>여자</label>
    </div>

</template>

<script>
export default {
    data() {
        return{
            gender : 'male'
        }
    }
}
</script>

<style>

</style>
<template>
    <div>
        <inpuut v-model="user.name"/>
    </div>
</template>

<script>
export default {
    data(){
        return {
            user : {
                name : ''
            }
        }
    },
    watch : {
        user(newVal, OldVal){
            console.log("user change!!")
        },
        deep :true

    }
}
</script>

<style>

</style>
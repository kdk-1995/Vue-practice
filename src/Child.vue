<template>
    <div>
        <h3>{{ title }}</h3>
        <p>{{ price }}원</p>
        <input type="number" v-model.number="quantity" @change="sendQuantity" placeholder="선택 수량을 입력해 주십시오" min="0" max="10"/> 
    </div>
</template>

<script>
export default {
    props : ['title', 'price'],
    data() {
        return {
            quantity : 0
        }
    },
    methods : {
        sendQuantity(){
            this.$emit('changelength',this.price, this.quantity)
        }
    }
}
</script>

<style>

</style>
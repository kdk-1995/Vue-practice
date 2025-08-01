<template>
    <div>
        <h3>{{ title }}</h3>
        <p>{{ price }}원</p>
        <input 
            type="number" 
            :value="modelValue"
            @input="updateQuantity"
            placeholder="선택 수량을 입력해 주십시오" 
            min="0" max="10"
        /> 
    </div>
</template>
<script>
export default {
    props : ['title', 'price', 'modelValue'],
    data() {
        return {
            quantity : 0
        }
    },
    methods : {
        updateQuantity(event){
            this.$emit('update:modelValue', Number(event.target.value));
            this.$emit('changed', this.price, Number(event.target.value));
        }
    }
}
</script>

<style>

</style>
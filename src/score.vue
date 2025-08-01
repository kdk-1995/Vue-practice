<template>
    <div>
        <input type="number" v-model.number="score" placeholder="점수를 입력하세요" />
        <p v-if="score >= 90">A</p>
        <p v-else-if="score >= 80">B</p>
        <p v-else-if="score >= 70">C</p>
        <p v-else>F</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            score : 0
        }
    }
}
</script>

<style>

</style>
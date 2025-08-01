<template>
    <SlotChild
    v-for="(student, index) in students"
    :key="index"
    :name="student.name"
    :grade="student.grade"
    >
    <template #studentInfo>
        <strong v-if="student.grade === 1" style="color:blue">1학년 신입생</strong>
        <strong v-else-if="student.grade === 3" style="color:red">3학년 졸업예정자</strong>
        <strong v-else style="color:green">일반 학생</strong>
    </template>
</SlotChild>
</template>

<script>
import SlotChild from './SlotC.vue'

export default {
   data(){
     return {
        students: [
            { name: '홍길동', grade: 1 },
            { name: '김영희', grade: 3 },
            { name: '박철수', grade: 2 }
        ]
     }
   },
   components : {
     SlotChild
   }
}
</script>

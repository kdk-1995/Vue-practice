<template>
    <h1>회원가입</h1>

    <button @click="selectTab='nameTab'">이름</button>
    <button @click="selectTab='genderTab'">성별</button>

    <KeepAlive>
        <component :is="selectTab"/> 
    </KeepAlive>
</template>

<script>
import { KeepAlive } from 'vue';
import nameTab from './KeepAliveChild1.vue'
import genderTab from './KeepAliveChild2.vue'
export default {
    components : {
        nameTab, 
        genderTab
    },
    data(){
        return {
            selectTab : 'nameTab'
        }
    }
}
</script>
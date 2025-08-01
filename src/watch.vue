<template>
  <input v-model="keyword" placeholder="검색어 입력"/>
  <p>검색어 : {{keyword}}</p>
</template>

<script>
export default {
    data(){
        return{
            keyword : ""
        }
    },
    watch : {
        keyword(newVal, OldVal){
            console.log("데이터 변경 !!")
            
            fetch(`/search?query=${encodeURIComponent(newVal)}`)
                .then(response => {
                    // response 별 처리 로직
                })
                .then(data =>{
                    // API 를 통해 서버에서 받아온 데이터 처리 로직
                })
                .catch(error => {
                    // 에러 처리 로직
                })
        }

    }
}
</script>

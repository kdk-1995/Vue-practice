<template>
  <p>책을 가지고 있습니까?</p>
  <span>{{publishedBooksMessage}}</span>
  <!--isActive 값이 true면 active라는 class를 적용 false 면 미적용-->
  <div :class="{active : isActive}">calss 바인딩</div>
</template>

<script>
export default {
    data(){
        return{
            author : {
                name : 'John Doe',
                books : [
                    'book1',
                    'book2',
                    'book3'
                ]
            },
            isActive : true
        }
    },
    computed : {
        publishedBooksMessage(){
            return this.author.books.length > 0 ? 'Yes': 'No'
        }
    }
}
</script>

<style>

</style>
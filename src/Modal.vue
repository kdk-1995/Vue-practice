<template>
  <h1>영화 소개</h1>
  <p>해리포터</p>
  <button @click="open=true">상세보기</button>

  <div>
    <Teleport to="body">
     <div v-if="open" class="modal-overlay" @click.self="open = false">
        <div v-if="open" class="modal">
            <h2>해리포터 상세 정보</h2>
            <p>마법과 모험의 세계로 떠나는 이야기입니다.</p>
            <button @click="open=false">닫기</button>
        </div>
      </div>  
    </Teleport>
  </div>
</template>

<script>
export default {
    data(){
        return {
            open : false
        }
    }
}
</script>

<style>
    .modal-overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 998;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .modal {
        background: white;
        padding: 20px;
        border-radius: 8px;
        width: 300px;
        z-index: 999;
    }
</style>
<template>
  <button @click="show = !show">toggle</button>
  <Transition>
    <p v-if="show">hello</p>
  </Transition>
</template>

<script>
export default {
    data(){
        return {
            show : true
        }
    }
}
</script>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
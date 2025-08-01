<template>
  <h1>Book List</h1>
  <div v-for="(value, key) in books" :key="key">
    <p>{{ key }}: {{ value.title }} - {{ value.author }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      books: {
        book1: { title: "해리포터", author: "조앤 롤링" },
        book2: { title: "1984", author: "조지 오웰" },
      },
    };
  },
};
</script>

<style>
</style>
<template>
  <div class="book-item" :style="{backgroundColor: book.color}">
    <h3>{{book.title}}</h3>
    <p>{{book.author}}</p>
  </div>
</template>

<script>
export default {
  name: "BookComponent",
  props: ["book"]
};
</script>

<style lang="scss" scoped>
.book-item {
  height: 250px;
  padding: 1rem;
  cursor: pointer;
  display: flex;
  color: #fff;
  flex-flow: column;
  border-radius: 3px;

  h3 {
    margin-top: auto;
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  p {
    font-size: 0.8rem;
  }
}
</style>
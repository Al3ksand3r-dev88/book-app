<template>
  <div class="home">
    <h1>8 Classic Childrens books</h1>
    <div class="books-container">
      <div v-for="book in books" :key="book.id">
        <router-link :to="{ name: 'Detail', params: { id: book.id, book } }">
          <BookComponent class="book-item" :book="book" />
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import BookComponent from "../components/BookComponent";
export default {
  name: "Home",
  components: { BookComponent },
  computed: {
    books() {
      return this.$store.state.books;
    }
  }
};
</script>

<style lang="scss" scoped>
h1 {
  margin: 1rem 0;
  font-size: 3rem;
}
.books-container {
  gap: 1rem;
  margin: auto;
  display: grid;
  max-width: 960px;
  grid-template-columns: repeat(4, 1fr);

  a {
    text-decoration: none;
  }
}
</style>

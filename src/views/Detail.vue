<template>
  <div class="book-detail">
    <router-link to="/" class="back-btn">
      <i class="fas fa-arrow-circle-left"></i>
    </router-link>
    <div class="wrapper">
      <section class="book-cover" :style="{backgroundColor: book.color}">
        <h1>{{book.title}}</h1>
        <p>{{book.author}}</p>
      </section>
      <section class="book-info">
        <div>
          <h1>{{book.title}}</h1>
          <p>{{book.author}}</p>
        </div>

        <article>
          <p>{{book.plot}}</p>
        </article>
        <ul class="info">
          <li>Audience: {{book.audience}}</li>
          <li>First published: {{book.year}}</li>
          <li>Pages: {{book.pages}}</li>
          <li>Publisher: {{book.publisher}}</li>
        </ul>
        <button>Oh, I want to read it!</button>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "Detail",
  props: ["book"]
};
</script>

<style lang="scss" scoped>
.book-detail {
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  display: flex;
  position: fixed;
  flex-flow: column;
  background: #333;
  align-items: center;
  justify-content: center;

  .back-btn {
    color: #fff;
    font-size: 3rem;
    margin-top: auto;
  }

  .wrapper {
    width: 100%;
    margin: auto;
    display: flex;
    max-width: 960px;
    justify-content: space-between;

    .book-cover,
    .book-info {
      color: #fff;
      width: 48%;
      height: 500px;
    }

    .book-cover {
      display: flex;
      padding: 1rem;
      flex-flow: column;

      h1 {
        margin-top: auto;
        font-size: 1.8rem;
        margin-bottom: 0.5rem;
      }

      p {
        font-size: 1.3rem;
      }
    }

    .book-info {
      display: flex;
      flex-flow: column;
      justify-content: space-between;

      h1 {
        font-size: 2.5rem;
        margin-bottom: 1rem;
      }
      p {
        font-size: 1.2rem;
      }
      .info {
        padding: 10px;
        background: #222;
        list-style: none;
        display: grid;
        gap: 1rem;
        grid-template-columns: repeat(2, 1fr);
      }

      button {
        width: 200px;
        border: none;
        padding: 10px;
        cursor: pointer;
        font-size: 1.2rem;
        text-align: center;
        border-radius: 5px;
      }
    }
  }
}
</style>
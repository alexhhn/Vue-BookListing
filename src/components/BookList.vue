<template>
  <div>
    <h1> {{title}} </h1>
    <ul>
      <book-item v-for="book in books" :book='book'></book-item>
    </ul>
  </div>
</template>

<script>
import BookItem from './BookItem';

export default {
  name: 'BookList',
  components: {
    BookItem,
  },
  data() {
    return {
      title: 'All Books',
      books: [
        { title: 'Self-Reliance', author: 'Ralph Waldo Emerson' },
        { title: 'American Gods', author: 'Neil Gaiman' },
        { title: 'Amusing Ourselves to Death', author: 'Neil Postman' },
      ],
    };
  },
};
</script>



Then, after book-item's v-for attribute, add a shorthand bind for :book and set it equal to book. This will pass the book to the book-item as a prop.

<style>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}
</style>



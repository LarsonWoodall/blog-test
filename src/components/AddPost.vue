<template>
  <div>
      <form @submit="AddPost">
          <input type="text" name="author" placeholder="who wrote this?">
          <input type="text" name="title" placeholder="this is a title bih">
          <input type="text" name="body" placeholder="lets write a lot of stuff">
          <input type="submit" value="submit" class="btn">
     </form>
  </div>
</template>

<script>
import uuid from 'uuid';
export default {
  name: "AddPost",
  data() {
      return {
           title: '',
           author: '',
           body: ''
      }
  },
  methods: {
      addTodo(e) {
          e.preventDefault();
          const newPost = {
              id: uuid.v4(),
              author: this.author,
              title: this.title,
              body: this.body
          }
          // send up to parent
          this.$emit('add-post', newPost);
      }
  }
}
</script>

<style scoped>
form {
    display: flex;
}

input[type="text"] {
    flex:10;
    padding: 5px;
}

input[sype="submit"] {
    flex: 2;
}

</style>
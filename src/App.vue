<template>
  <div id="app">
    <AddPost v-on:add-post="addPost"/>
    <BlogPosts v-bind:blogPostObjs="blogPostObjs"/>
  </div>
</template>

<script>
import BlogPosts from './components/BlogPosts';
import AddPost from './components/AddPost';

export default {
  name: 'app',
  components: {
    BlogPosts,
    AddPost
  },
  data(){
    return{
            blogPostObjs: [
              {
                id: 1,
                title: "Hello World",
                author: "Larson",
                body: "this is our first post, isn't it very very cool?"
              }
            ]
          }
  },
  methods: {
    AddPost(newPost){
      this.blogPostObjs = [...this.blogPostObjs, newPost];
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.btn {
  display: inline-block;
  border: none;
  background: #555;
  padding: 7px 20px;
  cursor: pointer;
}
</style>
<template>
  <div>
    <div v-bind:key="postObj.id" v-for="postObj in blogPostObjs">
      <BlogPostItem v-bind:postObj="postObj"/>
    </div>
  </div>
</template>

<script>
import BlogPostItem from './BlogPostItem.vue';
export default {
  name: 'BlogPosts',
  components: {
    BlogPostItem
  },
  props: ["blogPostObjs"]
}
</script>

<style scoped>

</style>
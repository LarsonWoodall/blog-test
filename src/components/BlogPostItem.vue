</style>
<template>
  <div>
      <p>{{"Written by: "+postObj.author}}</p>
      <h3>{{postObj.title}}</h3>
      <p>{{postObj.body}}</p>
  </div>
</template>

<script>
export default {
  name: 'BlogPostItem',
  props: ["postObj"]
}
</script>

<style scoped>

</style>
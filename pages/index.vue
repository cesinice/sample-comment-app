<template>
  <section class="container">
    <div>
      <post-comment></post-comment>
      <comments></comments>
    </div>
  </section>
</template>

<script>
  import PostComment from '~/components/CommentPost.vue'
  import Comments from '~/components/Comments.vue'

  export default {
    components: {
      PostComment,
      Comments
    }
  }
</script>

<style>

</style>

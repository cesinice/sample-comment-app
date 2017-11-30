<template>
  <section class="container">
    <div>
      <post-comment></post-comment>
    </div>
  </section>
</template>

<script>
import PostComment from '~/components/CommentPost.vue'

export default {
  components: {
    PostComment
  }
}
</script>

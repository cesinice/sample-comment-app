<template>
  <section class="container">
    <div class="box">
      <article class="media">
        <div class="media-content">
          <div class="content">
            <p>
              <strong>{{ comment.author }}</strong>
              <br>
              <textarea class="textarea">{{ comment.comment }}</textarea>
            </p>
          </div>
          <div class="field is-grouped">
            <p class="control">
              <a v-on:click="this.deleteComment()" class="button is-danger is-focused">
                Delete
              </a>
            </p>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<script>
  import axios from 'axios'

  export default {
    data () {
      return {}
    },
    props: ['comment'],

    methods: {
      deleteComment: function () {
        axios.delete('/comments/' + this.comment.id)
      }
    }
  }
</script>

<style>

</style>

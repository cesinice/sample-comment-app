<template>
  <div>
    <comment v-for="comment in comments"
             :comment="comment">
    </comment>
  </div>
</template>
<script>
  import Comment from '~/components/Comment.vue'
  import axios from 'axios'

  export default {
    components: {
      Comment
    },
    data () {
      return {
        comments: []
      }
    },
    methods: {
      getComments: function () {
        axios.get('/comments')
          .then(response => {
            this.comments = response.data
          })
      }
    },
    mounted () {
      this.getComments()
    }
  }
</script>

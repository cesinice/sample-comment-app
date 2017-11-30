<template>
  <section>

    <div class="field">
      <label class="label">Username</label>
      <div class="control has-icons-left">
        <input class="input" type="text" placeholder="Username" v-model="username">
        <span class="icon is-small is-left">
            <i class="fa fa-user"></i>
          </span>
      </div>

      <div class="card">
        <header class="card-header">
          <p class="card-header-title">
            Leave a comment below
          </p>
        </header>

        <div class="content">
          <div class="field">
            <div class="control">
        <textarea class="textarea is-medium"
                  type="text"
                  placeholder="Type text here..."
                  v-model="commentMessage"
        >
        </textarea>
            </div>
          </div>
        </div>
        <footer class="card-footer">
          <a href="#" v-on:click="postMessage(commentMessage)" class="card-footer-item">Post</a>
          <a href="#" v-on:click="cancel()" class="card-footer-item">Cancel</a>
        </footer>
      </div>
    </div>
  </section>

</template>

<script>
  import axios from 'axios'
  export default {
    data () {
      return {
        commentMessage: '',
        username: ''
      }
    },
    methods: {
      postMessage: function (message) {
        alert('Username ' + this.username + ' message ' + message)
        axios.post('/comments', {
          author: this.username,
          comment: this.commentMessage
        })
          .catch(function (error) {
            console.log(error)
          })
        this.cancel()
      },
      cancel: function () {
        this.commentMessage = ''
      }
    }
  }
</script>

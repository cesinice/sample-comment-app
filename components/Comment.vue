<template>
  <section class="container">
    <div class="box">
      <article class="media">
        <div class="media-content">
          <div class="content">
            <p>
              <strong>{{ author }}</strong>
              <br>
              <textarea class="textarea">{{ comment }}</textarea>
            </p>
          </div>
          <div class="field is-grouped">
            <p class="control">
              <a class="button is-link is-focused">
                Edit
              </a>
            </p>
            <p class="control">
              <a class="button is-danger is-focused">
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
  export default {
    components: {
    }
  }
</script>

<style>

</style>

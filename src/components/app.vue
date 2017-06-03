<template>
  <div>
    <header class="site-header jumbotron">
      <div class="container">
        <div class="row">
          <div class="col-xs-12"></div>

        </div>
      </div>
    </header>
    <div class="container">
      <add :add="add"></add>
      <list :comments="comments" :remove="remove"></list>
    </div>
  </div>
</template>
<script>
  import add from './add'
  import list from './list'

  export default {
    data () {
      return {
        comments: [
          {username: '浅浅', content: '好美的风景'},
          {username: '落落', content: '好喝的水'}
        ]
      }
    },

    methods: {
      add (comment) {
        this.comments.unshift(comment)
      },
      remove (comment) {
        this.comments.$remove(comment)
      }
    },

    components: {
      add, list
    }
  }

</script>
<style></style>

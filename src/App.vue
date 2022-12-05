<template>
  <div id="app">
    <TweetPosts/>
  </div>
</template>

<script>
import TweetPosts from './components/TweetPosts.vue';

export default {
  name: 'App',
  components: {
    TweetPosts
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

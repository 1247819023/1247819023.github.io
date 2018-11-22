<template>
  <div id="app">
			<center>
				<img src="./assets/logo.png" />
				<h2>自己聊天系列</h2>
			</center>
      <comment></comment>
  </div>
</template>

<script>
import Comment from './components/comment/comment-comp.vue'

export default {
  name: 'app',
  components: {
    Comment
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

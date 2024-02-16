<template>
  <div id="app">
    <ChatBox />
  </div>
</template>

<script>
import ChatBox from './components/ChatBox.vue';

export default {
  name: 'App',
  components: {
    ChatBox
  }
}
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>

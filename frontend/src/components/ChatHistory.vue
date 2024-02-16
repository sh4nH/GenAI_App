<template>
    <div class="chat-history">
      <ChatMessage v-for="(message, index) in messages" :key="index" :text="message.text" />
    </div>
  </template>
  
  <script>
  import ChatMessage from './ChatMessage.vue';
  
  export default {
    name: 'ChatHistory',
    components: {
      ChatMessage
    },
    props: {
      messages: {
        type: Array,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .chat-history {
    max-height: 300px;
    overflow-y: auto;
  }
  </style>
  
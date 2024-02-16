<template>
    <div class="chat-box">
      <ChatHistory :messages="messages" />
      <ChatInput @new-message="sendMessage" />
    </div>
  </template>
  
  <script>
  import ChatHistory from './ChatHistory.vue';
  import ChatInput from './ChatInput.vue';
  
  export default {
    components: {
      ChatHistory,
      ChatInput
    },
    data() {
      return {
        messages: []
      };
    },
    methods: {
      sendMessage(text) {
        this.messages.push({ text, isUser: true });
  
        // Send user message to backend and receive bot response

      }
    }
  }
  </script>
  
  <style>
  .chat-box {
    display: flex;
    flex-direction: column;
    height: 100%;
  }
  </style>
  
<template>
    <div class="chat-input">
      <input type="text" v-model="message" @keyup.enter="sendMessage" placeholder="Type your message..." />
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        message: ''
      };
    },
    methods: {
      sendMessage() {
        if (this.message.trim() !== '') {
          this.$emit('new-message', this.message);
          this.message = '';
        }
      }
    }
  }
  </script>
  
  <style>
  .chat-input input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  </style>
  
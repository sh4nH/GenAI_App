<template>
    <div class="message">
      <p>{{ text }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChatMessage',
    props: {
      text: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .message {
    margin-bottom: 10px;
  }
  </style>
  
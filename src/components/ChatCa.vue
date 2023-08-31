<template>
    <div class="chat">
      <ChatMessage
        v-for="(message, index) in messages"
        :key="index"
        :message="message"
      />
    </div>
  </template>

  <script>
  import ChatMessage from './ChatMessage.vue';

  export default {
    components: {
      ChatMessage,
    },
    data() {
      return {
        messages: [
          { text: 'Oi! Como você está?', isSent: true },
          { text: 'Oi! Estou bem, obrigado!', isSent: false },
          { text: 'E como foi o seu dia?', isSent: true },
          { text: 'Foi ótimo! Fui ao parque.', isSent: false },
          // ... mais mensagens aqui ...
        ],
      };
    },
  };
  </script>

  <style scoped>
  .chat {
    width: 800px;
    height: 600px;
    overflow-y: scroll;
    box-shadow: 1px;
    border: 1px solid #ccc;
    float: right;
}
  </style>

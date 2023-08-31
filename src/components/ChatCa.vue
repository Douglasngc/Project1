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
    props:{
      navbarOpen: Boolean,
    },
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
          { text: 'Oi! Como você está?', isSent: true },
          { text: 'Oi! Estou bem, obrigado!', isSent: false },
          { text: 'E como foi o seu dia?', isSent: true },
          { text: 'Foi ótimo! Fui ao parque.', isSent: false },
          { text: 'Oi! Como você está?', isSent: true },
          { text: 'Oi! Estou bem, obrigado!', isSent: false },
          { text: 'E como foi o seu dia?', isSent: true },
          { text: 'Foi ótimo! Fui ao parque.', isSent: false },
          { text: 'Oi! Como você está?', isSent: true },
          { text: 'Oi! Estou bem, obrigado!', isSent: false },
          { text: 'E como foi o seu dia?', isSent: true },
          { text: 'Foi ótimo! Fui ao parque.', isSent: false },
          { text: 'Oi! Como você está?', isSent: true },
          { text: 'Oi! Estou bem, obrigado!', isSent: false },
          { text: 'E como foi o seu dia?', isSent: true },
          { text: 'Foi ótimo! Fui ao parque.', isSent: false },
          // ... mais mensagens aqui ...
        ],
      };
    },
    computed: {
      contentStyles() {
        return {
          
          
          marginLeft: this.navbarOpen ? '260px' : '0',
          transition: 'margin-left 0.3s',
        };
      },
    },
  };
  </script>

  <style scoped>
  .chat {

  padding: 20px;
  transition: margin-left 0.3s; /* Adiciona uma transição suave */
    width: 700px;
    height: 610px;
    overflow-y: scroll;
   background-image: url(https://images.pexels.com/photos/7791111/pexels-photo-7791111.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1);
  background-size: cover;
   
    border: 1px solid #ccc;
    float: right;
}
::-webkit-scrollbar {
  width: 8px; /* Largura da barra de rolagem */
}

::-webkit-scrollbar-thumb {
  background-color: #d1d1d1; /* Cor do polegar da barra de rolagem */
  border-radius: 4px; /* Borda arredondada do polegar */
}

::-webkit-scrollbar-track {
  background-color: #f0f0f0; /* Cor da faixa de trilha */
}

/* Barra de rolagem horizontal (caso necessário) */
::-webkit-scrollbar-horizontal {
  height: 8px; /* Altura da barra de rolagem horizontal */
}

::-webkit-scrollbar-thumb:horizontal {
  background-color: #d1d1d1; /* Cor do polegar da barra de rolagem horizontal */
  border-radius: 4px; /* Borda arredondada do polegar horizontal */
}

::-webkit-scrollbar-track:horizontal {
  background-color: #f0f0f0; /* Cor da faixa de trilha horizontal */
}
  </style>

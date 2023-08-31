<template>
  <div class="message" :class="{ 'sent': isSent, 'received': !isSent }">
    <div class="message-content">
      <div class="avatar">
        <img :src="isSent ? sentAvatar : receivedAvatar" alt="Avatar" />
      </div>
      <div class="message-bubble">
        {{ message.text }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: Object,
      required: true,
    },
  },
  computed: {
    isSent() {
      return this.message.isSent;
    },
    sentAvatar() {
      return require('@/assets/sent-avatar.png'); // Caminho da imagem para mensagens enviadas
    },
    receivedAvatar() {
      return require('@/assets/received-avatar.png'); // Caminho da imagem para mensagens recebidas
    },
  },
};
</script>

<style scoped>
.message {
  margin: 10px 0;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 100%;
}

.received {
  align-items: flex-start;
}

.sent {
  align-items: flex-end;
}

.message-content {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.avatar {
  width: 40px;
  height: 40px;
  margin-right: 10px;
}

.avatar img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
}

.message-bubble {
  border-radius: 10px;
  padding: 10px;
  max-width: 70%;
  word-wrap: break-word;
  background-color: #f0f0f0;
}

.received .message-bubble {
  background-color: #e0e0e0;
}

.sent .message-bubble {
  background-color: #007bff;
  color: white;
}
</style>

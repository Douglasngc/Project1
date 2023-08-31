<template>
    <div>


      <div class="content" :style="contentStyles">
<div class="scroll">
        <div class="notes">
          <div v-for="index in 10" :key="index" class="card">
            <p><strong>Nome:</strong> Douglas</p>
            <p><strong>Idade:</strong> 13</p>
            <p><strong>Estado:</strong> Fortaleza</p>
          </div>
        </div>
      </div>
      </div>
    </div>
  </template>

  <script>
  export default {
    props: {
      navbarOpen: Boolean,
    },
    computed: {
      contentStyles() {
        return {
          marginTop: '100px',
          marginLeft: this.navbarOpen ? '260px' : '0',
          transition: 'margin-left 0.3s',
        };
      },
    },
  };
  </script>
 <style scoped>
 .content {
  margin-top: 100px;
  padding: 30px;
  transition: margin-left 0.3s; /* Adiciona uma transição suave */
}

  .notes {
    margin-top:-100px;
    max-height: 550px;
    max-width: 350px;
    overflow-y: scroll;
  }

  .card {
    background-color: #ff7f34;
    border: 1px solid #ddd;
    padding: 10px;
    margin-bottom: 10px;
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
::-webkit-scrollbar {
  width: 0; /* Largura da barra de rolagem */
  height: 0; /* Altura da barra de rolagem */
}
</style>

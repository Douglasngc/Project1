<template>
    <div>


      <div class="content" :style="contentStyles">

        <div class="notes">
          <div v-for="index in 10" :key="index" class="card">
            <p><strong>Nome:</strong> Douglas</p>
            <p><strong>Idade:</strong> 13</p>
            <p><strong>Estado:</strong> Fortaleza</p>
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
    max-height: 555px;
    max-width: 300px;
    overflow-y: scroll;
  }

  .card {
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    padding: 10px;
    margin-bottom: 10px;
  }
</style>

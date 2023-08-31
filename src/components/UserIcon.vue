<template>
    <div class="user-icon" @click="toggleDropdown">
      <div class="user-icon-img">
        <img src="../assets/6596121.png" alt="User Icon">
      </div>
      <div v-if="dropdownOpen" class="dropdown">
        <p><strong>Nome:</strong> {{ username }}</p>
        <p><a @click="logout">Fazer logout</a></p>
      </div>
    </div>
  </template>

  <script>
  export default {
    data() {
      return {
        dropdownOpen: false,
        username: 'Douglas', // Nome do usuário
      };
    },
    methods: {
      toggleDropdown() {
        this.dropdownOpen = !this.dropdownOpen;
      },
      logout() {
        // Lógica para fazer logout
        console.log('Fazendo logout...');
      },
    },
  };
  </script>

  <style scoped>
  .user-icon {
    position: relative;
    cursor: pointer;
    display: flex;
    align-items: center;
  }

  .user-icon-img {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    overflow: hidden;
    margin-right: 10px;
  }

  .user-icon-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .dropdown {
    position: absolute;
    top: 100%;
    right: 0;
    background-color: #fff;
    border: 1px solid #ccc;
    padding: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    z-index: 1000;
  }

  .dropdown p {
    margin: 5px 0;
  }

  .dropdown a {
    color: #007bff;
    cursor: pointer;
  }
  </style>

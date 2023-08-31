<template>
    <div>
      <div>
        <div @click="toggleMenu" class="toggle-button">
          <span class="menu-icon" :class="{ 'open': isOpen }">&#9776;</span>
        </div>
        <div class="side-menu" :class="{ 'active': isOpen }">
          <ul>
            <li>Sobre nós</li>
            <li>Chat</li>
            <li>Cards</li>
          </ul>
        </div>
      </div>
    </div>
  </template>

  <script>
  export default {
    data() {
      return {
        isOpen: false,
      };
    },
    methods: {
      toggleMenu() {
        this.isOpen = !this.isOpen;
        this.$emit('toggleMenu', this.isOpen); // Emitindo evento com estado do menu
      },
    },
  };
  </script>

  <style scoped>
  .side-menu {
    width: 250px;
    background-color: #f1f1f1;
    position: fixed;
    top: 0;
    left: -250px;
    height: 100%;
    transition: left 0.3s;
    margin-top: 50px;
    padding: 30px;

  }

  .side-menu.active {
    left: 0;
  }

  .toggle-button {
    margin-top: -15px;
    background:none;
    border: none;
    color: #333;
    cursor: pointer;
    display: flex;
    align-items: center;
    position: fixed;
    top: 20px;
    left: 20px;
    z-index: 1000;
  }

  .menu-icon {
    font-size: 24px; /* Ajuste o tamanho conforme necessário */
    transition: transform 0.3s;
  }

  .menu-icon.open {
    transform: rotate(90deg);
  }

  ul {
    list-style: none;
    padding: 0;
    margin-top: 20px;
  }

  li {
    margin-bottom: 10px;
    cursor: pointer;
  }
  .navbar{
    background-color: rgba(0, 0, 0, 0.2);
  }
  </style>

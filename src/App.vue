<template>
  <div>
    <body>
      
   
     <AppTopBar />
    <AppNavbar @toggleMenu="toggleNavbar" />
<ChatCa />
    <AppCards :navbarOpen="navbarOpen" />
  </body>
  </div>
</template>

<script>
import AppTopBar from './components/AppTopBar.vue';

import AppCards from './components/AppCards.vue';
import ChatCa from './components/ChatCa.vue';
import AppNavbar from './components/AppNavbar.vue';
export default {
  components: {
    AppNavbar,
    AppCards,
    AppTopBar,
    ChatCa
  },
  data() {
    return {
      navbarOpen: false,
    };
  },
  methods: {
    toggleNavbar(isOpen) {
      this.navbarOpen = isOpen; // Atualizar o estado do menu
    },
  },
};
</script>

<style scoped>
body{
  background-image: url(./assets/slider-2.png);
  background-size: cover;
}

</style>



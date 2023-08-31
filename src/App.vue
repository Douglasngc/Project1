<template>
  <div>
    <AppTopBar />
    <AppNavbar @toggleMenu="toggleNavbar" />
    <AppCards :navbarOpen="navbarOpen" />
  </div>
</template>

<script>
import AppTopBar from './components/AppTopBar.vue';
import AppCards from './components/AppCards.vue';
import AppNavbar from './components/AppNavbar.vue';
export default {
  components: {
    AppNavbar,
    AppCards,
    AppTopBar,
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


</style>



<template>
    <div class="top-bar">
        <div class="spacer"></div>
      <div class="logo">

        <!-- Coloque sua logo aqui -->
        <img src="../assets/logo.png" alt="Logo">
      </div>
      <UserIcon />
    </div>
  </template>

  <script>
  import UserIcon from './UserIcon.vue';
  export default {
    components:{
        UserIcon,
    }
    // Component logic, methods, etc.
  };
  </script>

  <style scoped>
  .top-bar {
    background-color: #f1f1f1;
    height: 50px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 0 20px;

  }

  .logo {
    margin-right: 20px;

  }

  .logo img {
    float:left;
    max-height: 40px;

    /* Adjust other styles for the logo image */
  }
  .spacer {
    flex-grow: 0;
  }
  </style>

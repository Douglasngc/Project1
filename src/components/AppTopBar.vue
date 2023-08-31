<template>
    <div class="top-bar">
        <div class="spacer"></div>
      <div class="logo">

        <!-- Coloque sua logo aqui -->
        <img src="../assets/logo.png" alt="Logo">
      </div>

    </div>
  </template>

  <script>
  export default {
    // Component logic, methods, etc.
  };
  </script>

  <style scoped>
  .top-bar {
    background-color: rgba(0, 0, 0, 0.2);
    height: 50px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 0 20px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
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

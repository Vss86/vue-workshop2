<template>
    <div>
      <header>
        <slot name="header"></slot>
      </header>
      <main>
        <slot name="main"></slot>
      </main>
      <footer>
        <slot name="footer"></slot>
      </footer>
    </div>
  </template>
  
  <script lang="ts">
  export default {
  };
  </script>
  
  <style scoped>
  div {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }
  
  header {
    background-color: #333;
    color: white;
    padding: 10px;
  }
  
  main {
    flex-grow: 1;
  }
  
  footer {
    background-color: #333;
    color: white;
    padding: 10px;
  }
  </style>
  
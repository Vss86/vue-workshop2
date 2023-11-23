<template>
    <div class="card">
      <h2>{{ cardTitle }}</h2>
      <p>{{ cardContent }}</p>
      <button @click="notifyParent">Klicka här</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['cardTitle', 'cardContent'],
    methods: {
      notifyParent() {
        this.$emit('card-clicked', { title: this.cardTitle, content: this.cardContent });
      },
    },
  };
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    padding: 15px;
    margin: 10px;
    border-radius: 5px;
    background-color: #f9f9f9;
  }
  
  button {
    margin-top: 10px;
    padding: 5px 10px;
    cursor: pointer;
  }
  </style>
  
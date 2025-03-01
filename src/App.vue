<template>
    <div>
      <h2>Вызов функций из родительского компонента</h2>
      <!-- Передаем две функции в дочерний компонент -->
      <employee 
        :firstFunction="firstFunction" 
        :secondFunction="secondFunction"
      ></employee>
    </div>
  </template>
  
  <script>
  import Employee from './Employee.vue'; // Импортируем дочерний компонент
  
  export default {
    components: {
      Employee // Регистрируем дочерний компонент
    },
    methods: {
      // Первая функция
      firstFunction() {
        alert('Первая функция вызвана!');
      },
      // Вторая функция
      secondFunction() {
        alert('Вторая функция вызвана!');
      }
    }
  }
  </script>
  
  <style scoped>
  h2 {
    color: #333;
  }
  </style>
  
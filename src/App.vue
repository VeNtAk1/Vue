<template>
    <div>
      <h2>Информация о работнике</h2>
      <!-- Передаем данные в дочерний компонент -->
      <employee :name="workerName" :salary="workerSalary" :age="workerAge"></employee>
    </div>
  </template>
  
  <script>
  import Employee from './Employee.vue'; // Импортируем дочерний компонент
  
  export default {
    components: {
      Employee // Регистрируем дочерний компонент
    },
    data() {
      return {
        // Данные работника, которые передаем в дочерний компонент
        workerName: 'Иван Иванов',
        workerSalary: 50000,
        workerAge: 30
      };
    }
  };
  </script>
  
  <style scoped>
  h2 {
    color: #333;
  }
  </style>
  
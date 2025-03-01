<template>
    <div>
      <h2>Список работников</h2>
      <!-- Цикл v-for для создания компонента Employee для каждого работника -->
      <employee
        v-for="user in users"
        :key="user.id"
        :name="user.name"
        :salary="user.salary"
        :age="user.age"
      ></employee>
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
        // Массив работников
        users: [
          {
            id: 1,
            name: 'name1',
            salary: 100,
            age: 30,
          },
          {
            id: 2,
            name: 'name2',
            salary: 200,
            age: 40,
          },
          {
            id: 3,
            name: 'name3',
            salary: 300,
            age: 50,
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  h2 {
    color: #333;
  }
  </style>
  
<template>
    <div>
      <p>Имя: {{ user.name }}</p>
      <p>Зарплата: {{ user.salary }}</p>
      <p>Возраст: {{ user.age }}</p>
      <!-- Кнопка для удаления работника -->
      <button @click="deleteEmployee">Удалить работника</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      // Пропс для получения данных работника
      user: {
        type: Object,
        required: true
      },
      // Пропс для метода удаления работника
      removeUser: {
        type: Function,
        required: true
      }
    },
    methods: {
      // Метод для вызова удаления работника
      deleteEmployee() {
        // Передаем id работника для удаления
        this.removeUser(this.user.id);
      }
    }
  };
  </script>
  
  <style scoped>
  button {
    margin-top: 10px;
    padding: 5px 10px;
    cursor: pointer;
  }
  </style>
  
<template>
    <div>
      <h2>Список элементов</h2>
      <!-- Передаем массив в дочерний компонент -->
      <child-component :items="elementsList"></child-component>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue'; // Импортируем дочерний компонент
  
  export default {
    components: {
      ChildComponent // Регистрируем дочерний компонент
    },
    data() {
      return {
        // Массив, который будем передавать в дочерний компонент
        elementsList: ['Элемент 1', 'Элемент 2', 'Элемент 3', 'Элемент 4']
      };
    }
  };
  </script>
  
  <style scoped>
  h2 {
    color: #333;
  }
  </style>
  
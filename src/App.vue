<template>
    <div>
      <h3>Информация о работнике</h3>
      <p>Имя: {{ workerName }}</p>
      <!-- Кнопка для передачи имени работника в родительский компонент -->
      <button @click="sendWorkerName">Отправить имя в родительский компонент</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      // Принимаем метод из родительского компонента через пропс
      sendName: {
        type: Function,
        required: true
      }
    },
    data() {
      return {
        // Имя работника
        workerName: 'John Doe'
      };
    },
    methods: {
      // Метод, который вызывает метод родителя и передает имя работника
      sendWorkerName() {
        this.sendName(this.workerName); // Вызываем переданный метод и передаем имя работника
      }
    }
  }
  </script>
  
  <style scoped>
  h3 {
    color: #333;
  }
  button {
    padding: 10px;
    cursor: pointer;
  }
  </style>
  
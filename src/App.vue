<template>
    <div>
      <template v-if="!isEdit">
        <!-- Режим отображения данных -->
        <p>{{ user.name }} {{ user.surname }}</p>
        <button @click="edit">Редактировать</button>
      </template>
      <template v-else>
        <!-- Режим редактирования -->
        <input v-model="newName" />
        <input v-model="newSurname" />
        <button @click="save">Сохранить</button>
      </template>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: {
        type: Object,
        required: true,
      },
    },
    data() {
      return {
        isEdit: false, // Флаг редактирования
        newName: this.user.name, // Новый name
        newSurname: this.user.surname, // Новый surname
      };
    },
    methods: {
      edit() {
        // Включаем режим редактирования
        this.isEdit = true;
      },
      save() {
        // Сохраняем изменения и возвращаемся в режим отображения
        this.isEdit = false;
        const updatedUser = {
          ...this.user,
          name: this.newName,
          surname: this.newSurname,
        };
        this.$emit('updateUser', updatedUser); // Отправляем обновленные данные в родительский компонент
      },
    },
  };
  </script>
  
  <style scoped>
  input {
    margin-right: 5px;
  }
  button {
    margin-top: 10px;
  }
  </style>
  
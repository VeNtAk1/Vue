<template>
    <tr :key="user.id">
      <td>{{ user.name }}</td>
      <td>{{ user.salary }}</td>
      <td>{{ user.age }}</td>
      <td>
        <a href="#" @click.prevent="removeUser">Удалить</a>
      </td>
      <td>
        <a href="#" @click.prevent="editUser">Редактировать</a>
      </td>
    </tr>
  </template>
  
  <script>
  export default {
    props: {
      user: Object
    },
    methods: {
      removeUser() {
        this.$emit("remove", this.user.id); // Отправляем событие с id работника для удаления
      },
      editUser() {
        this.$emit("edit", this.user); // Отправляем событие с данными работника для редактирования
      }
    }
  }
  </script>
  
  <style scoped>
  a {
    color: blue;
    cursor: pointer;
  }
  a:hover {
    text-decoration: underline;
  }
  </style>
  
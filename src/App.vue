<template>
    <div>
      <table border="1">
        <thead>
          <tr>
            <th>Имя</th>
            <th>Фамилия</th>
            <th>Возраст</th>
            <th>Удалить</th>
            <th>Редактировать</th>
          </tr>
        </thead>
        <tbody>
          <employee
            v-for="user in users"
            :key="user.id"
            :firstName="user.firstName"
            :lastName="user.lastName"
            :age="user.age"
            :userId="user.id"
            @remove="removeUser"
            @edit="editUser"
          ></employee>
        </tbody>
      </table>
  
      <!-- Форма редактирования -->
      <div v-if="editingUser">
        <h3>Редактирование пользователя</h3>
        <form @submit.prevent="saveUser">
          <div>
            <label for="firstName">Имя:</label>
            <input type="text" id="firstName" v-model="updatedFirstName">
          </div>
          <div>
            <label for="lastName">Фамилия:</label>
            <input type="text" id="lastName" v-model="updatedLastName">
          </div>
          <div>
            <label for="age">Возраст:</label>
            <input type="number" id="age" v-model="updatedAge">
          </div>
          <button type="submit">Сохранить изменения</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  import Employee from './Employee.vue'; // Импортируем компонент
  
  export default {
    components: {
      Employee // Регистрируем компонент
    },
    data() {
      return {
        users: [
          {
            id: 1,
            firstName: 'name1',
            lastName: 'surname1',
            age: 30,
          },
          {
            id: 2,
            firstName: 'name2',
            lastName: 'surname2',
            age: 40,
          },
          {
            id: 3,
            firstName: 'name3',
            lastName: 'surname3',
            age: 50,
          },
        ],
        editingUser: null,
        updatedFirstName: '',
        updatedLastName: '',
        updatedAge: ''
      };
    },
    methods: {
      removeUser(id) {
        this.users = this.users.filter(user => user.id !== id); // Удаляем работника по id
      },
      editUser(user) {
        this.editingUser = user;
        this.updatedFirstName = user.firstName;
        this.updatedLastName = user.lastName;
        this.updatedAge = user.age;
      },
      saveUser() {
        if (this.editingUser) {
          this.editingUser.firstName = this.updatedFirstName;
          this.editingUser.lastName = this.updatedLastName;
          this.editingUser.age = this.updatedAge;
          this.editingUser = null; // Закрываем форму редактирования
        }
      }
    }
  };
  </script>
  
  <style scoped>
  table {
    width: 100%;
    border-collapse: collapse;
  }
  th,
  td {
    padding: 10px;
    text-align: left;
  }
  form {
    margin-top: 20px;
  }
  form div {
    margin-bottom: 10px;
  }
  </style>
  
<script>
export default {
    data() {
        return {
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
                },
            ],
            editingUser: null, // Переменная для хранения редактируемого работника
            updatedName: '',
            updatedSalary: '',
            updatedAge: ''
        }
    },
    methods: {
        removeUser(id) {
            this.users = this.users.filter(user => user.id !== id); // Удаляем работника по id
        },
        editUser(user) {
            this.editingUser = user;
            this.updatedName = user.name;
            this.updatedSalary = user.salary;
            this.updatedAge = user.age;
        },
        saveUser() {
            if (this.editingUser) {
                this.editingUser.name = this.updatedName;
                this.editingUser.salary = this.updatedSalary;
                this.editingUser.age = this.updatedAge;
                this.editingUser = null; // Закрываем форму редактирования
            }
        }
    }
}
</script>

<template>
    <table border="1">
        <thead>
            <tr>
                <th>Имя</th>
                <th>Зарплата</th>
                <th>Возраст</th>
                <th>Удалить</th>
                <th>Редактировать</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in users" :key="user.id">
                <td>{{ user.name }}</td>
                <td>{{ user.salary }}</td>
                <td>{{ user.age }}</td>
                <td>
                    <a href="#" @click.prevent="removeUser(user.id)">Удалить</a>
                </td>
                <td>
                    <a href="#" @click.prevent="editUser(user)">Редактировать</a>
                </td>
            </tr>
        </tbody>
    </table>

    <!-- Форма редактирования -->
    <div v-if="editingUser">
        <h3>Редактирование пользователя</h3>
        <form @submit.prevent="saveUser">
            <div>
                <label for="name">Имя:</label>
                <input type="text" id="name" v-model="updatedName">
            </div>
            <div>
                <label for="salary">Зарплата:</label>
                <input type="number" id="salary" v-model="updatedSalary">
            </div>
            <div>
                <label for="age">Возраст:</label>
                <input type="number" id="age" v-model="updatedAge">
            </div>
            <button type="submit">Сохранить изменения</button>
        </form>
    </div>
</template>

<style>
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        padding: 10px;
        text-align: left;
    }
    a {
        color: blue;
        cursor: pointer;
    }
    a:hover {
        text-decoration: underline;
    }
    form {
        margin-top: 20px;
    }
    form div {
        margin-bottom: 10px;
    }
</style>

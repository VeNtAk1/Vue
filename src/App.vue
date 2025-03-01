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
        }
    },
    methods: {
        removeUser(id) {
            this.users = this.users.filter(user => user.id !== id); // Удаляем работника по id
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
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in users" :key="user.id">
                <td>{{ user.name }}</td>
                <td>{{ user.salary }}</td>
                <td>{{ user.age }}</td>
                <td>
                    <a href="#" @click.prevent="removeUser(user.id)">Удалить</a> <!-- При клике удаляется работник -->
                </td>
            </tr>
        </tbody>
    </table>
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
        color: red;
        cursor: pointer;
    }
    a:hover {
        text-decoration: underline;
    }
</style>

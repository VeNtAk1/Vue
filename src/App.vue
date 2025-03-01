<script>
export default {
    data() {
        return {
            items: ['Первый элемент', 'Второй элемент', 'Третий элемент'], // Исходный массив
            inputText: '' // Текст, введённый в инпут
        }
    },
    methods: {
        addItem() {
            if (this.inputText.trim() !== '') { // Проверяем, не пустой ли введённый текст
                this.items.push(this.inputText); // Добавляем новый элемент в массив
                this.inputText = ''; // Очищаем инпут после добавления
            }
        }
    }
}
</script>

<template>  
    <ul>
        <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>

    <input type="text" v-model="inputText" placeholder="Введите текст">
    <button @click="addItem">Добавить в список</button>
</template>

<style>
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        margin: 5px 0;
    }
    input {
        margin-right: 10px;
    }
</style>

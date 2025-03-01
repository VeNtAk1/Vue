<script>
export default {
    data() {
        return {
            inputText: '', // Текст из инпута
            savedText: ''  // Текст, который будет отображаться
        }
    },
    methods: {
        saveText(event) {
            if (event.key === 'Enter') { // Проверяем, нажата ли клавиша Enter
                this.savedText = this.inputText; // Сохраняем введённый текст
                this.inputText = ''; // Очищаем поле ввода
            }
        }
    }
}
</script>

<template>  
    <input type="text" v-model="inputText" @keyup.enter="saveText" placeholder="Введите текст и нажмите Enter">
    <p v-if="savedText">Вы ввели: {{ savedText }}</p>
</template>

<style>
    input {
        display: block;
        margin-bottom: 10px;
        padding: 5px;
    }
</style>

<script>
export default {
    data() {
        return {
            message: '' // Текст, который будет отображаться
        }
    },
    methods: {
        handleClick(event) {
            if (event.ctrlKey) { // Проверяем, зажат ли Ctrl
                event.preventDefault(); // Предотвращаем переход по ссылке
                this.message = 'Вы нажали на ссылку с зажатым Ctrl!';
            }
        }
    }
}
</script>

<template>  
    <a href="https://example.com" @click="handleClick">Нажмите на меня с Ctrl</a>
    <p v-if="message">{{ message }}</p>
</template>

<style>
    a {
        display: block;
        margin-bottom: 10px;
        color: blue;
        cursor: pointer;
        text-decoration: underline;
    }
</style>

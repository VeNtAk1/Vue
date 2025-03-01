<script>
export default {
    data() {
        return {
            isDisabled: false // Флаг блокировки инпута
        }
    },
    methods: {
        toggleInput() {
            this.isDisabled = !this.isDisabled; // Меняем состояние блокировки
        }
    }
}
</script>

<template>  
    <input type="text" :disabled="isDisabled" placeholder="Введите текст...">
    <button @click="toggleInput">
        {{ isDisabled ? 'Разблокировать' : 'Заблокировать' }}
    </button>
</template>

<style>
    input {
        display: block;
        margin-bottom: 10px;
        padding: 5px;
    }
</style>

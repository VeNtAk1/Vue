<script>
export default {
    data() {
        return {
            selectedDay: '', // Переменная для хранения выбранного дня
            days: ['Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота', 'Воскресенье'] // Список дней недели
        }
    }
}
</script>

<template>  
    <p>Выберите день недели:</p>

    <select v-model="selectedDay">
        <option disabled value="">-- Выберите день --</option>
        <option v-for="day in days" :key="day" :value="day">{{ day }}</option>
    </select>

    <p v-if="selectedDay">Вы выбрали: {{ selectedDay }}</p>
</template>

<style>
    select {
        display: block;
        margin-top: 10px;
    }
</style>

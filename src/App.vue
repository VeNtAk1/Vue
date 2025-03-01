<script>
export default {
    data() {
        return {
            selectedDay: '',
            selectedMonth: '',
            selectedYear: '',
            days: Array.from({ length: 31 }, (_, i) => i + 1), // Список дней 1-31
            months: [
                'Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 
                'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'
            ],
            years: Array.from({ length: 100 }, (_, i) => new Date().getFullYear() - i) // Последние 100 лет
        }
    }
}
</script>

<template>  
    <p>Выберите дату:</p>

    <label>День:
        <select v-model="selectedDay">
            <option disabled value="">-- День --</option>
            <option v-for="day in days" :key="day" :value="day">{{ day }}</option>
        </select>
    </label>

    <label>Месяц:
        <select v-model="selectedMonth">
            <option disabled value="">-- Месяц --</option>
            <option v-for="month in months" :key="month" :value="month">{{ month }}</option>
        </select>
    </label>

    <label>Год:
        <select v-model="selectedYear">
            <option disabled value="">-- Год --</option>
            <option v-for="year in years" :key="year" :value="year">{{ year }}</option>
        </select>
    </label>

    <p v-if="selectedDay && selectedMonth && selectedYear">
        Вы выбрали: {{ selectedDay }} {{ selectedMonth }} {{ selectedYear }} года
    </p>
</template>

<style>
    select {
        display: block;
        margin: 5px 0;
    }
</style>

<script>
export default {
    data() {
        return {
            selectedCity: '', // Переменная для хранения выбранного города
            cities: ['Москва', 'Санкт-Петербург', 'Новосибирск', 'Екатеринбург', 'Казань'] // Список городов
        }
    }
}
</script>

<template>  
    <p>Выберите ваш город:</p>

    <select v-model="selectedCity">
        <option disabled value="">-- Выберите город --</option>
        <option v-for="city in cities" :key="city" :value="city">{{ city }}</option>
    </select>

    <p v-if="selectedCity">Вы живете в: {{ selectedCity }}</p>
</template>

<style>
    select {
        display: block;
        margin-top: 10px;
    }
</style>

<script>
export default {
    data() {
        return {
            selectedLanguage: '', // Переменная для хранения выбранного языка
            languages: ['Русский', 'Английский', 'Французский', 'Немецкий', 'Испанский'] // Список языков
        }
    }
}
</script>

<template>  
    <p>Какой язык для вас родной?</p>

    <label v-for="lang in languages" :key="lang">
        <input type="radio" v-model="selectedLanguage" :value="lang"> {{ lang }}
    </label>

    <p v-if="selectedLanguage">Ваш родной язык: {{ selectedLanguage }}</p>
</template>

<style>
    label {
        display: block;
    }
</style>

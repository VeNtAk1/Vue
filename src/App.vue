<script>
export default {
    data() {
        return {
            selectedLanguages: [], // Массив для хранения выбранных языков
            languages: ['JavaScript', 'Python', 'C++', 'Java', 'PHP'] // Список языков
        }
    }
}
</script>

<template>  
    <p>Какие языки программирования вы знаете?</p>
    
    <label v-for="lang in languages" :key="lang">
        <input type="checkbox" v-model="selectedLanguages" :value="lang"> {{ lang }}
    </label>

    <p v-if="selectedLanguages.length">Вы знаете: {{ selectedLanguages.join(', ') }}</p>
</template

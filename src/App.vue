<script>
export default {
    data() {
        return {
            items: ['Первый элемент', 'Второй элемент', 'Третий элемент'] // Исходный массив
        }
    },
    methods: {
        removeItem(index) {
            this.items.splice(index, 1); // Удаляем элемент по индексу
        }
    }
}
</script>

<template>  
    <ul>
        <li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
            {{ item }}
        </li>
    </ul>
</template>

<style>
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        margin: 5px 0;
        cursor: pointer;
        color: blue;
    }
    li:hover {
        text-decoration: underline;
    }
</style>

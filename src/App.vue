<script>
export default {
    data() {
        return {
            day: "Пятница", // пусть сейчас там 3
        }
    },
    methods:{
       
    },
}
</script>


<template>
    <p v-if="day === 'Понедельник' ">Понедельник</p>
    <p v-if="day === 'Вторник' ">Вторник</p>
    <p v-if="day === 'Среда' ">Среда</p>
    <p v-if="day === 'Четверг' ">Четверг</p>
    <p v-if="day === 'Пятница' ">Пятница</p>
    <p v-if="day === 'Суббота' ">Суббота</p>
    <p v-if="day === 'Воскресенье' ">Воскресенье</p>
</template>

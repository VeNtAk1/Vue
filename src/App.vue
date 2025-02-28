<script>
export default {
    data() {
        return {
            age: 25, 
        }
    },
    methods:{
       
    },
}
</script>


<template>
   <p v-if=" age < 18">Подросток</p>
   <p v-if=" 19 < age < 25">Молодой человек</p>
   <p v-if=" age > 26">Мужчина</p>
</template>

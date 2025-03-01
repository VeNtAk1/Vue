<script>
export default {
    data() {
        return {
            text: '',
            binar: false,
        }
    },
    methods:{
        show(){
            this.binar = !this.binar;
        }   
    }
}
</script>


<template>  
    <textarea v-model="text"></textarea>
    <button @click="show">Нажми</button>
    <ul v-if="binar">
        <li v-for="elem in text">{{ elem }}</li>
    </ul>
</template>

<style>
    
</style>

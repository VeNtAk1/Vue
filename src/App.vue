<script>
export default {
    data() {
        return {
            message: null,
        }
    },
    methods:{
       show(){
        this.message = this.message**2;
       }
    }
}
</script>


<template>  
    <input v-model="message" type="number">
    <button @click="show">Нажми</button>
    <p>{{ messages }}</p>
</template>

<style>
    
</style>

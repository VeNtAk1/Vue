<script>
export default {
    data() {
        return {
            message_1: null,
            message_2: null,
        }
    },
    methods:{
       show(){
        if (this.message_1 != this.message_2){
            this.message_2 = this.message_1;
        }
        else{
            this.message_1 = this.message_2;
        }
       }
    }
}
</script>


<template>  
    <input v-model="message_1" type="text">
    <br>
    <input v-model="message_2" type="text">
    <button @click="show">Нажми</button>
</template>

<style>
    
</style>

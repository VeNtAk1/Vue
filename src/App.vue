<script>
export default {
    data() {
        return {
            message: "hello",
        }
    },
    methods:{
       show(){

       }
    }
}
</script>


<template>
     {{ message}}
    <input v-model="message"  type="text">
    <br>    
   

</template>

<style>
    
</style>

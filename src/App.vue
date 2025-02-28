<script>
export default {
    data() {
        return {
            binar: false,
        }
    },
    methods:{
        show(){
            this.binar = !this.binar
        }
    }
}
</script>


<template>
    <div v-if="binar">
        <p>+</p>
        <p>+</p>
        <p>+</p>
    </div>
   <button @click="show">Нажми на меня</button>
</template>

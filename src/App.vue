<script>
export default {
    data(){
        return{
            visible_1: true,
            visible_2: true,
            visible_3: true,
        }
    },
    methods:{
        toggle_1(){
            this.visible_1 = !this.visible_1;
        },
        toggle_2(){
            this.visible_2 = !this.visible_2;
        },
        toggle_3(){
            this.visible_3 = !this.visible_3;
        }
    },
}
</script>


<template>
    <p v-if="visible_1">text1</p>
    <p v-if="visible_2">text_2</p>
    <p v-if="visible_3">text_3</p>
    <button @click="toggle_1">button_1</button>
    <button @click="toggle_2">button_2</button>
    <button @click="toggle_3">button_3</button>
</template>

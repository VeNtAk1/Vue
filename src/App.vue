<script>
export default {
    data(){
        return{
            visible: false,
            visible_button_1: true,
            visible_button_2: false,
        }
         
    },
    methods:{ 
        hide(){
            this.visible =  true
            this.visible_button_1 = false
            this.visible_button_2 = true
        },
        hide_2(){
            this.visible = false
            this.visible_button_2 = false
            this.visible_button_1 = true


        }

    }
}
</script>


<template>
    <p v-if="visible">text_1</p>
    <button @click="hide" v-if="visible_button_1">Появись</button>
    <button @click="hide_2"  v-if="visible_button_2">Уберись</button>
</template>

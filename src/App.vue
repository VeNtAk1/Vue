<script>
export default {
    data(){
        return{
            visible: false,
        }
         
    },
    methods:{ 
        hide(){
            this.visible =  true
        },
        hide_2(){
            this.visible = false
        }
    }
}
</script>


<template>
    <p v-if="visible">text_1</p>
    <button @click="hide" style="margin: 10px;">Появись</button>
    <button @click="hide_2" style="margin: 10px;">Уберись</button>
</template>

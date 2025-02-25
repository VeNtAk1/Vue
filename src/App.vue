<script>
export default {
    data(){
        return {
            visible_1: true,
            visible_2: false,
        }  
    },
    methods:{  
       
    }
}
</script>


<template>
    <p v-if="visible_1">text_1</p>
    <p v-if="visible_2">text_2</p>
</template>

<script>
export default {
    data(){
        return {
            hidden: "text",
        }  
    },
    methods:{  
       
    }
}
</script>


<template>
    <p v-if="!hidden">text_1</p>
</template>

<script>
export default {
    data(){
        return{
            isAuth: true, 
        }
    },
    methods:{
       
    },
}
</script>


<template>
    <p v-if="isAuth">+++</p>
	<p v-else>---</p>
</template>

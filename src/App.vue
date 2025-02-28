<script>
export default {
    data() {
        return {
            isActive: true,
		    isDisabled: true,
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <p :class="{active: isActive, disable: isDisabled}">text</p>
</template>
<style>
    
</style>

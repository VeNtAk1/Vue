<script>
import NewComponent from './NewComponent.vue'
export default{
    data() {
	    return {
		    num1: 1,
		    num2: 2,
	    };
    },
    methods: {
    show: function(){
        alert(this.num1 + this.num2)
        }
    },
    mounted() {
        this.show();
    }
};
</script>
<template>

</template>
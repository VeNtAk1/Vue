<script>
export default {
    data() {
        return {
            binar: false,
        }
    },
    methods:{
        toggle(){
                this.binar = !this.binar
        }
    }
}
</script>


<template>
    <p v-show="binar">text</p>
    <button @click="toggle">click</button>
</template>

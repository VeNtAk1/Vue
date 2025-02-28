<script>
export default {
    data() {
        return {
            arr: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
        }
    },
    methods:{
       show(){
        this.arr.push(11)
       },
       firstdel(){
        this.arr.shift()
       }
    }
}
</script>


<template>
    <p>3rgr</p>
</template>
<style>
    p {
        color: green;
    }
</style>

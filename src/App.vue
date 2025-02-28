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
    <!-- <button @click="show">Нажми на меня</button>
    <p>{{ arr }}</p> -->
    <button @click="firstdel">Удали</button>
    {{ arr }}
</template>

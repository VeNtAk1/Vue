<script>
export default {
    data() {
        return {
            arr: [1, 2, 3, 4, 5]
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <!-- <p v-for="elem in arr">{{ elem }} </p> -->
    <!-- <p v-for="elem in arr">{{ elem**2 }} </p> -->
    <ul>
        <li v-for="elem in arr">{{ elem }}</li>
    </ul>
</template>

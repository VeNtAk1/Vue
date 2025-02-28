<script>
export default {
    data() {
        return {
            items: [1, -2, 3, -4, 5],
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <div v-for="elem in items">
        <p v-if="elem > 0">{{ elem }}</p>
    </div>

</template>

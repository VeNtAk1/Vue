<script>
export default {
    data() {
        return {
            arr: {user1: "100$", user2: "200$", user3: "300$"},
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <ul>
        <li v-for="(elem, key) in arr">{{ elem }}</li>
        <hr>
        <li v-for="(elem, key) in arr">{{ key }} - {{ elem }}</li>
        <hr>
        <li v-for="(elem, key, index) in arr">{{ key }} - {{ elem }} - {{ index }}</li>
        <hr>
        <li v-for="(elem, key, index) in arr">{{ key }} - {{ elem }} - {{ index + 1 }}</li>

    </ul>

</template>

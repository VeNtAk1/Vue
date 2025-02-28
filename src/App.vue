<script>
export default {
    data() {
        return {
            items: [1, 2, 3],
        }
    },
    methods:{
       
    }
}
</script>


<template>
    <div v-for="elem in items">
        {{ elem }}
        <p class="divider"></p>
    </div>
    <ul v-for="elem in items">
        <li>{{ elem }}</li>
        <li class="divider"></li>
    </ul>
</template>

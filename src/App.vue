<script>
export default {
    methods:{  
        first(){
            alert("Gh")
        }
    }
}
</script>


<template>
    <a @click.stop>Нажми на меня</a>
    <a @click.once="first">Нажми на меня_#2</a>
</template>

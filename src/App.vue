<script>
import NewComponent from './NewComponent.vue'
export default{
  methods:{
    show: function(){
      alert("18.02.2025")
    }
  }
}
</script>
<template>
  <button v-on:click="show">text</button>
  <button @mouseover="show">text_2</button>
</template>
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
  {{ show() }}
</template>
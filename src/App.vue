<script>
import NewComponent from './NewComponent.vue'
export default{
  data() {
    return {
      num1: 1,
      num2: 2,
    }
  },
  methods: {
    show:function(a,b){
      alert(a + b)
    }
  }
}
</script>
<template>
  {{ show(num1, num2) }}
</template>
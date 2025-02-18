<script>
import NewComponent from './NewComponent.vue'
export default{
  data() {
    return {
      num: 5,
      num1: 1,
      num2: 2,
      num3: 3,
    }
  }
  
}
</script>
<template>
  {{ num*num }}
  <br>
  {{ num1 + num2 + num3 }}
</template>
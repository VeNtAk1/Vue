<script>
import NewComponent from './NewComponent.vue'
export default{
  data() {
    return {
      arr: ['x', 'y', 'z'],
      result: [1, 2, 3]
    }
  }
}
</script>
<template>
  {{ arr[0] }}
  {{ arr[1] }}
  {{ arr[2] }}
  <br>
  {{ result[0] + result[1] + result[2] }}
</template>
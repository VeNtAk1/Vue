<script>
import NewComponent from './NewComponent.vue'
export default{
  data() {
    return {
      name: 'john',
      surn: 'smit',
    }
  }
}
</script>
<template>
  <div>{{ name }} </div>
  <div> {{ surn }}</div>
</template>
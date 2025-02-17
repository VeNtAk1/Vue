<script>
import NewComponent from './NewComponent.vue'
export default{
  data() {
    return {
      text: 'page',
      href: 'page.html',
    }
  }
}
</script>
<template>
  <a><img :src="href" alt="">{{ text }}</a>
</template>
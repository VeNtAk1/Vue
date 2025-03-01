<template>
    <div>
      <ChildComponent @show="handleShowEvent" />
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent
    },
    methods: {
      handleShowEvent(param1, param2) {
        // Здесь вы можете обработать переданные параметры
        console.log(param1, param2);  // Выведет 'xxx' и 'yyy'
      }
    }
  }
  </script>
  
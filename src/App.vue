<script>
export default {
  data() {
    return {
      inputNumber: null,  // Ввод пользователя
    };
  },
  methods: {
    // Метод для вычисления квадрата числа
    showSquare(number) {
      if (number || number === 0) { // Проверяем, что введено число
        alert(`Квадрат числа равен ${number * number}`);
      } else {
        alert("Пожалуйста, введите число.");
      }
    }
  }
};
</script>

<template>
  <div>
    <input v-model.number="inputNumber" type="number" placeholder="Введите число">
    <br>
    <button @click="showSquare(inputNumber)">
      Показать квадрат числа
    </button>
    <br>
    <button @click="showSquare(2)">
      Показать квадрат числа
    </button>
    <br>
    <button @click="showSquare(3)">
      Показать квадрат числа 3
    </button>
  </div>
</template>

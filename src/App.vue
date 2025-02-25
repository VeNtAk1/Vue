<script>
export default {
  data() {
    return {
      inputNumber: null,  // Ввод пользователя
      dayOfWeek: '',      // Результат для дня по числу
      currentDay: '',     // Результат для текущего дня
    };
  },
  methods: {
    // Метод для получения дня недели по числу
    getDayOfWeek(number) {
      const days = ["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"];
      
      if (number >= 1 && number <= 7) {
        this.dayOfWeek = days[number - 1]; // Возвращаем день недели, уменьшая на 1
      } else {
        this.dayOfWeek = "Пожалуйста, введите число от 1 до 7.";
      }
    },
    // Метод для получения текущего дня недели
    getCurrentDay() {
      const days = ["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"];
      const currentDayIndex = new Date().getDay(); // Метод getDay() возвращает индекс дня недели от 0 до 6
      this.currentDay = days[currentDayIndex];
    }
  },
  mounted() {
    this.getCurrentDay();  // Вызываем метод сразу после монтирования компонента, чтобы отобразить текущий день
  }
};
</script>
<template>
    <div>
      <input v-model.number="inputNumber" type="number" placeholder="Введите число от 1 до 7">
      <button @click="getDayOfWeek(inputNumber)">
        Получить день недели
      </button>
      <p v-if="dayOfWeek">День недели по номеру: {{ dayOfWeek }}</p>
      <p>Сегодняшний день недели: {{ currentDay }}</p>
    </div>
</template>
<script setup>
import Calculator from './components/Calculator.vue';
import Question from './components/Question.vue';
import RandomTextGenerator from './components/RandomTextGenerator.vue';
</script>

<template>
  <Question />
  <div class="flex justify-around gap-2">
    <Calculator />
    <RandomTextGenerator />
  </div>
</template>

<style scoped></style>

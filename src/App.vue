<script setup>
import Calculator from './components/Calculator.vue';
import RandomTextGenerator from './components/RandomTextGenerator.vue';
</script>

<template>
  <div class="text-center bg-slate-300">
    <h1 class="text-3xl font-bold underline ">
      Assignment-02
    </h1>

    <h2 class="text-2xl 800 ">Calculator and Text Generation</h2>
    <h3>Submitted By Sabbasachi Saha</h3>
    <hr>
  </div>
  <div class="question w-2/3 text-justify p-5 m-5 ">
    <h2 class="text-2xl font-weight underline ">Question:</h2>
    Develop a web application using Vue 3 with the following functionalities:
    <p>
      <span class="font-bold">Create a calculator with basic arithmetic operations (+, -, *, /). Implement this
        functionality within a separate
        component named 'Calculator'.</span>
    <ul class="list-[upper-roman]"> The calculator component should consist of:
      <li>Two input fields for entering numeric values.</li>
      <li>One input field for selecting the arithmetic operation (+, -, *, /).</li>
      <li>Upon submission, display the result below the submit button.</li>
    </ul>
    <hr>
    </p>
    <p>
      <span class="font-bold">Implement a separate component to fetch and display data from an API.
        Utilize the following API: https://animechan.xyz/api/random</span>
      <br>
      This API returns a JSON object with the following format:<br>
      <code>
                            {<br>
                            id: "",<br>
                            quote: "",<br>
                            anime: "",<br>
                            character: ""<br>
                            }</code><br>
      Display the retrieved JSON object data.


      Note: The provided API generates random text upon each call, so keep this in mind during development to avoid
      confusion.
    </p>
  </div>
  <div class="flex justify-between gap-2">
    <Calculator />
    <RandomTextGenerator />
  </div>
</template>

<style scoped></style>

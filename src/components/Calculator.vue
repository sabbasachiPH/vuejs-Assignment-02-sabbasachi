<script setup>
import { ref, reactive } from "vue";

const firstNumber = ref(0);
const secondNumber = ref(0);
const operation = ref("");
const result = ref(0);

function handleSubmit() {
    if ('+' === operation.value) {
        result.value = firstNumber.value + secondNumber.value
    } else if ('-' === operation.value) {
        result.value = firstNumber.value - secondNumber.value
    } else if ('*' === operation.value) {
        result.value = firstNumber.value * secondNumber.value
    } else if ('/' === operation.value) {
        result.value = firstNumber.value / secondNumber.value
    } else {
        result.value = "Something Wrong. Please Check"
    }
}

function handleSwitchSubmit() {
    switch (operation.value) {
        case '+':
            result.value = firstNumber.value + secondNumber.value;
            break;
        case '-':
            result.value = firstNumber.value - secondNumber.value;
            break;
        case '*':
            result.value = firstNumber.value * secondNumber.value;
            break;
        case '/':
            result.value = firstNumber.value / secondNumber.value;
            break;
        default:
            result.value = "Something Wrong. Please Check"
    }

}

</script>
<template>
    <div class="bg-red-100 flex-1">
        <h2 class="text-2xl p-5 text-center font-bold">Calculator</h2>
        <!-- 
        <div class="text-center text-3xl">
            {{ firstNumber }} {{ operation }} {{ secondNumber }} = {{ result }}
        </div> -->
        <div class="inputs flex">
            <input v-model="firstNumber" class="m-3 p-5 bg-blue-200" type="number" placeholder="First Number"
                required="required" id="">

            <select v-model="operation" class="m-3 p-5 bg-blue-200" id="">
                <option disabled value="">Please select one</option>
                <option>+</option>
                <option>-</option>
                <option>*</option>
                <option>/</option>
            </select>
            <input v-model="secondNumber" type="number" class="m-3 p-5 bg-blue-200" placeholder="Second Number"
                required="required" id="">
            <!-- <input @click="handleSubmit" type="button" value="Calculate" class="m-3 p-5 bg-green-300"> -->
            <button @click="handleSubmit" type="submit" class="m-3 p-5 bg-green-300">Calculate</button>
            <button @click="handleSwitchSubmit" type="submit" class="m-3 p-5 bg-green-300">Calculate Switch</button>
        </div>


        <p class="m-3 p-5 text-2xl font-black bg-gray-400 w-1/2">
            Result: {{ result }}
        </p>

    </div>
</template>



<style lang="scss" scoped></style>
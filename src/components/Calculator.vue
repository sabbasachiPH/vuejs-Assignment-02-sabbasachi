<script setup>

</script>
<template>
    <div class="bg-red-100 flex-1">
        <h2 class="text-2xl p-5 text-center font-bold">Calculator</h2>
        <input name="firstNum" class="m-5 p-5 bg-blue-200" type="number" placeholder="First Number" required="required"
            id="">
        <select name="operation" class="m-5 p-5 bg-blue-200" id="">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
        <input type="number" name="secondNum" class="m-5 p-5 bg-blue-200" placeholder="Second Number" required="required"
            id="">
        <input type="button" value="Calculate" class="m-5 p-5 bg-green-300">
        <p class="m-5 p-5 text-2xl font-black bg-gray-400 w-1/2">
            Result:
        </p>

    </div>
</template>



<style lang="scss" scoped></style>
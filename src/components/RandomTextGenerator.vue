<script setup>
import { ref, reactive } from 'vue';

const text = reactive(
    {
        id: "1",
        quote: "The real me is super cool!",
        anime: "Katekyo Hitman Reborn!",
        character: "Reborn"
    }
);
async function fetchData() {
    try {
        const response = await fetch('https://animechan.xyz/api/random');
        const data = await response.json();
        text.id = data.id;
        text.quote = data.quote;
        text.anime = data.anime;
        text.character = data.character;
    } catch (error) {
        console.error(error);
    }
}



</script>
<template>
    <div class="flex-1">
        <h2 class="text-2xl p-5 text-center font-bold">Random Text Generator</h2>
        <div class="shadow hover:shadow-lg p-5">
            <blockquote class="relative">
                <div class="relative z-10">
                    <p class="text-gray-800 sm:text-xl "><em>
                            {{ text.quote }}
                        </em></p>
                </div>
            </blockquote>
            <cite class="mt-6 text-base font-semibold text-gray-400">
                -- {{ text.character }} ( {{ text.anime }})
            </cite>
        </div>
        <hr>
        <button @click="fetchData" class="m-5 p-5 bg-green-300">Click Here to Find Next Quote</button>
    </div>
</template>



<style lang="scss" scoped></style>
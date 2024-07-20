<script setup>
import { defineProps } from 'vue';
import { RouterLink } from 'vue-router';
const { quizQuestionLength, numberOfCorrectAnswer } = defineProps([
    "quizQuestionLength",
    "numberOfCorrectAnswer"
])
</script>
<template>
    <section class="result">
        <p>Score: </p>
        <h1>{{ numberOfCorrectAnswer }}/{{ quizQuestionLength }}</h1>
        <RouterLink to="/">Go Back</RouterLink>
    </section>
</template>

<style scoped>
.result {
    text-align: center;
    padding: 10px 0;
}

p{
    font-size: 25px;
}

h1{
    font-size: 80px
}
</style>
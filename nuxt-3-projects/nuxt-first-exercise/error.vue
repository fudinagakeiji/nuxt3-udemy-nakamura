<template>
    <div v-if="error.statusCode === 404">
    <h1>error!</h1></div>
    <p>{{ error.message }}</p>
</template>
<script setup>
const error = useError()
</script>
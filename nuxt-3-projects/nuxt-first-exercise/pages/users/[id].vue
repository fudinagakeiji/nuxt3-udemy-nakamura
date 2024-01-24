<template>
    <div>
        <h1>id page</h1>
        <p>users/{{ $route.params.id }}を表示中</p>
        <hr>
        <nuxtLink to="/">top</nuxtLink>
    </div>
</template>

<script setup>
definePageMeta({
    validate: async(route) => {
        return /^\d+$/.test(route.params.id)
    }
})
</script>
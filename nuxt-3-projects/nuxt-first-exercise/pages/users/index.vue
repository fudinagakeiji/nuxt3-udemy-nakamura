<template>
    <div>
        <h1>usersのindex page</h1>
        <p>routingはusers/</p>
        {{ counter }}
        <!-- <img src="/assets/cat.jpg" alt=""> -->
        <hr>
        <nuxtLink to="/">top</nuxtLink>
    </div>
</template>
<script setup>
// import { useCountState } from "~/composables";

const counter = useCountState()
</script>

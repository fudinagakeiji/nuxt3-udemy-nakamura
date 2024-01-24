<template>
    <div>
        <h1>Top page</h1>
        <!-- useStateの値：　{{ title }} -->
        <!-- <button @click="$event => titleState.changeTitle('hello Nuxt3!!!!')">changeTitle!!!!</button> -->
        <h1>{{ counter }}</h1>
        <button @click="counterStore.countUp">+</button>
        <button @click="counterStore.countDown">-</button>
        <button @click="counterStore.Reset">Reset</button>
        <hr>
        <nuxtLink to="/price">price</nuxtLink>
    </div>
</template>
<script setup>
// const title = useState('title',()=> 'hello keijiii!')
// const title = useTitle()
// const titleState = useTitle()
// const {title} = titleState

const counterStore = useCounterState()
const {counter}  = counterStore
</script>
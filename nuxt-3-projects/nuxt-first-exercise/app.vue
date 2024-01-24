<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
      <!-- <p>{{ users[0].id }}, {{ users[0].name }} </p> -->
      <ul>
        <li v-for="user in users" :key="user.id">
          {{ user.id }}, {{ user.name }}
        </li>
      </ul>
    </NuxtLayout>
  </div>
</template>
<script setup>
// const {data: users, error} = await useFetch('https://jsonplaceholder.typicode.com/userss')
const {data: users, error} = await useFetch('https://jsonplaceholder.typicode.com/users')
console.log(error.value)
if(error.value) {
  throw createError({statusCode: 404, statusMessage: 'page not found......'})
}
useHead(
  {
    title: 'nuxt3勉強中',
    link:[
      {rel:"stylesheet", href:"https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap"}
    ]

  }
)</script>

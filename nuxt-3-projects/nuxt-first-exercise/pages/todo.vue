<template>
  <div>
    <h1>To DO</h1>
    <div>
      <form @submit.prevent="addTask">
        <input v-model="newTask" name="newTask" autocomplete="off"/>
        <button>Add</button>
      </form>
      <ul>
        <li v-for="(task, index) in tasks" :key="task">
          <span>{{task  }}  </span>
          <button @click="$event=> deleteTask(index)">  delete</button>
        </li>
      </ul>
      <button @click="clearTask">clear</button>
    </div>
    <hr />
    <nuxtLink to="/">top</nuxtLink>
  </div>
  <!-- </NuxtLayout> -->
</template>
<script setup>
const tasks = useCookie(
  'tasks',
  {
    default: () => []
  }
)
const newTask = ref('')
function addTask(){
  if(newTask.value.length >= 1){
    tasks.value.push(newTask.value)
  }
  newTask.value = ''
}
function deleteTask(index) {
  tasks.value.splice(index, 1)
}
function clearTask() {
  tasks.value = []
}
</script>

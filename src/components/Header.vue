<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @btn-click="$emit('toggle-add-task')" :text="addTaskbuttonChange ? 'Close' : 'Add Task'" :color="addTaskbuttonChange ? 'red' : 'green'" />
    </header>
</template>

<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
       title: String,
       addTaskbuttonChange: Boolean,
      },
      components: {
        Button
      },
    }  
    
</script>

<style scoped>
 header {
     display: flex;
     justify-content: space-between;
     align-items: center;
     margin-bottom: 20px;
 }
</style>
<template>
   <header>
      <h1>{{ title }}</h1>
      <Button 
      @btn-click="$emit
      ('toggle-add-task-btn')" 
      color="pink" 
      :text="showAddTask ? 'Close' : 'Add Task'"/>
   </header>
</template>

<script>
import Button from './Button.vue'

export default {
   name:'Header',
   props: {
      title: String,
      showAddTask: Boolean
   },
   components: {
      Button
   }
}
</script>

<style scoped>
   header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1em;
   }
</style>
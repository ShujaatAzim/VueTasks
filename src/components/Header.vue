<template>
  <header>
    <h1>{{ title }}</h1>
    <Button 
      @btn-click="$emit('btn-click')" 
      :text="showForm ? 'Close' : 'Add Task'" 
      :color="showForm ? 'red' : 'green'" 
    />
  </header>
</template>

<script>
  import Button from './Button'

  export default {
    name: "Header",
    components: {
      Button
    },
    props: {
      title: String,
      showForm: Boolean
    }
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

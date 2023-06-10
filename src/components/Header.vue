<script setup>
defineProps({
  Header: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1>{{ Header }}</h1>
  </div>
</template>

<style scoped>

</style>

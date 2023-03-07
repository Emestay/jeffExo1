<template>
    <div class="bg-gray-100 p-4 rounded-lg">
      <h2 class="text-lg font-medium mb-2">{{ user.name }}</h2>
      <p class="text-gray-700">Age: {{ user.age }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: {
        type: Object,
        required: true
      }
    }
  }
  </script>
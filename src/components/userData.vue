<template>
    <div class="bg-gray-100 p-4 rounded-lg">
      <div class="mb-4">
        <label class="block text-gray-700 font-medium mb-2">Nom:</label>
        <input v-model="name" type="text" class="border rounded-lg p-2 w-full" placeholder="Rentre ton nom">
      </div>
      <div class="mb-4">
        <label class="block text-gray-700 font-medium mb-2">Age:</label>
        <input v-model.number="age" type="number" class="border rounded-lg p-2 w-full" placeholder="Puis ton age">
      </div>
      <button class="bg-blue-500 text-white rounded-lg px-4 py-2" @click="updateData">MAJ de la data</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        age: null
      }
    },
    methods: {
      updateData() {
        if (!this.name || !this.age) {
          alert('Deconne pas, remplis moi')
          return
        }
  
        this.$emit('update', {
          name: this.name,
          age: this.age
        })
  
        this.name = ''
        this.age = null
      }
    }
  }
  </script>
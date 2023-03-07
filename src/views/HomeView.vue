<template>
  <div class="container mx-auto">
    <h1 class="text-2xl font-medium mb-4">Info du User</h1>
    <div class="grid grid-cols-2 gap-4">
      <active-user :user="user"></active-user>
      <user-data @update="updateUser"></user-data>
    </div>
  </div>
</template>

<script>
import ActiveUser from '../components/activeUser.vue'
import UserData from '../components/userData.vue'

export default {
  components: {
    ActiveUser,
    UserData
  },
  data() {
    return {
      user: {
        name: 'Jésus',
        age: 33,
      }
    }
  },
  methods: {
    updateUser(data) {
      this.user.name = data.name
      this.user.age = data.age
    }
  }
}
</script>
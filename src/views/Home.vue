<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <UserAdminDashboard></UserAdminDashboard>
  </div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue'
import UserAdminDashboard from '@/components/UserAdminDashboard.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    UserAdminDashboard
  }
}
</script>

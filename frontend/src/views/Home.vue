<script setup>
import Dashboard from '@/components/Dashboard.vue'
import Login from '@/components/Login.vue'
import Nav from '@/components/Nav.vue'
import { ref } from 'vue'

let loggedIn = ref(false)

function setLogin(login_bool) {
  loggedIn.value = login_bool
}
</script>

<template>
  <div class="main-con">
    <Nav />
    <Dashboard v-if="loggedIn" class="dashboard" />
    <Login v-else class="login" @login-bool="setLogin" />
  </div>
</template>

<style scoped lang="scss">
.main-con {
  display: flex;
  flex-direction: column;
  height: 100vh;

  .dashboard,
  .login {
    flex-grow: 1;
    overflow-y: auto;
  }
}
</style>

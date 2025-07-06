<script setup>
import { ref } from 'vue'

const emit = defineEmits(['login-bool'])

let password = ref('')

function login() {
  if (password.value == '1234') {
    emit('login-bool', true)
  }
}
</script>

<template>
  <div class="main-con">
    <div class="j-circle">
      <h2>Hello Sir!</h2>
      <p>"Please Login"</p>
    </div>
    <div class="login-con">
      <div class="password-con">
        <label for="password">Password</label>
        <input type="text" name="password" class="password" v-model="password" />
      </div>
      <button class="login-btn" @click="login">Login</button>
    </div>
  </div>
</template>
<style scoped lang="scss">
.main-con {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #000;

  .j-circle {
    background: transparent;
    border-radius: 100rem;
    aspect-ratio: 1/1;
    padding: 3rem;
    border: solid var(--navy-blue);
    border-width: 0.5rem;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h2 {
      font-size: 3rem;
      padding: 1rem;
    }
    p {
      font-size: 1.5rem;
      padding: 1rem;
    }
  }

  .login-con {
    color: white;
    padding: 3rem;
    margin: 1rem;
    font-size: 2rem;
    border: solid var(--navy-blue);
    border-radius: 50rem;
    border-width: 0.3rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    align-items: center;

    .password-con {
      display: flex;
      justify-content: center;
      gap: 1rem;

      input {
        border-radius: 12rem;
        padding-left: 0.8rem;
        max-width: 14rem;
        font-size: 2rem;
      }
    }

    .login-btn {
      max-width: 12rem;
      font-size: 2rem;
      padding: 0.5rem 1.5rem;
      border-radius: 2rem;
      border: solid var(--navy-blue);
      border-width: 0.3rem;
      color: white;
      background: transparent;
    }
  }
}
</style>

<script setup></script>

<template>
  <div class="main-con">
    <div class="login-con">
      <h2>Hello Sir!</h2>
      <p>"Please Login"</p>
    </div>
  </div>
</template>
<style scoped lang="scss">
.main-con {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #000;

  .login-con {
    background: transparent;
    border-radius: 100rem;
    aspect-ratio: 1/1;
    padding: 3rem;
    border: solid white;
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
}
</style>

<script setup lang="ts">
function openURL(url: string) {
  window.open(url);
}
</script>

<template>
  <div class="e-nuxt-container">
    <h1 class="title text-3xl font-semibold text-arubaGreen pt-5">Electron Test App</h1>
    <div class="e-nuxt-content">
      <div class="e-nuxt-logo">
        <img style="max-width: 100%" src="../assets/electron.png" alt="electron icon" />
      </div>
      <div class="e-nuxt-system-info bg-gray-100">
        <Header msg="test" />
        <Counter />
        <router-view />
      </div>
    </div>
    <div class="e-nuxt-links">
      <div class="e-nuxt-button" @click="openURL('https://github.com/michalzaq12/electron-nuxt')">Github</div>
      <div class="e-nuxt-button" @click="openURL('https://nuxtjs.org/guide')">Nuxt.js</div>
      <div class="e-nuxt-button" @click="openURL('https://electronjs.org/docs')">Electron.js</div>
    </div>
  </div>
</template>

<style>
.e-nuxt-container {
  min-height: calc(100vh - 50px);
  background: linear-gradient(to right, #ece9e6, #ffffff);
  font-family: Helvetica, sans-serif;
}

.e-nuxt-content {
  display: flex;
  justify-content: space-around;
  padding-top: 50px;
  align-items: flex-start;
  flex-wrap: wrap;
}

.e-nuxt-logo {
  width: 400px;
}

.e-nuxt-system-info {
  padding: 20px;
  border-top: 1px solid #397c6d;
  border-bottom: 1px solid #397c6d;
}

.e-nuxt-links {
  padding: 25px 0;
  display: flex;
  justify-content: center;
}

.e-nuxt-button {
  color: #364758;
  padding: 5px 20px;
  border: 1px solid #397c6d;
  margin: 0 20px;
  border-radius: 15px;
  font-size: 1rem;
}

.e-nuxt-button:hover {
  cursor: pointer;
  color: white;
  background-color: #397c6d;
}
</style>

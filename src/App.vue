<template>
  <nav class="app">
    <router-link to="/">Home</router-link> &nbsp;
    <router-link to="/about">About</router-link> &nbsp;
    <router-link to="/project">Projects</router-link> &nbsp;
    <router-link to="/contact">Contact</router-link> &nbsp;
  </nav>
  <router-view v-slot="{ Component }">
  <transition name="fade" mode="out-in">
  <component :is="Component" />
  </transition>
  </router-view>
</template>

<style>

.app {
  text-align: center;
  font-size: 20px;
  letter-spacing: 3px;
}
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
  background: black;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
}

nav a.router-link-exact-active {
  color: #00b7ff;
}

nav a:hover {
  background: rgba(15, 30, 245, 0.425);
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s ease-out;
}
</style>

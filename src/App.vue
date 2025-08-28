<template>
  <div id="app">
    <NavBar />

    
    <main class="page-wrapper">
      <hero-section />
      <About />
      <Services />
      <Contact />
      <GetButton />
    </main>
  </div>
</template>

<script lang="ts" setup>
import NavBar from "./components/NavBar.vue";
import HeroSection from "./components/HeroSection.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Contact from "./components/Contact.vue";
import GetButton from "./components/GetButton.vue";
</script>

<style>

html {
  scroll-behavior: smooth; /* smooth scroll */
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Main wrapper for sections */
.page-wrapper {
  flex: 1;
  width: 100%;
  display: flex;
  flex-direction: column;
  margin-top: 88px;
}
section[id] {
  scroll-margin-top: 100px; /* same or slightly larger than navbar height */
}
</style>

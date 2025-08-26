<template>
  <div id="app">
    <NavBar />

    <!-- Full-width sections -->
    <main class="page-wrapper">
      <About />
      <Services />
      <Contact />
      <GetButton />
    </main>
  </div>
</template>

<script lang="ts" setup>
import NavBar from "./components/NavBar.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Contact from "./components/Contact.vue";
import GetButton from "./components/GetButton.vue";
</script>

<style>
/* Reset & global rules */
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

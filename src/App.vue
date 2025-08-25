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
import NavBar from './components/NavBar.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Contact from './components/Contact.vue'
import GetButton from './components/GetButton.vue'
</script>

<!-- <style>
/* Reset & global rules */
html, body, #app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}

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
}

/* Each section fills full width, min 100vh */
.page-wrapper > section {
  width: 100%;
  min-height: 100vh;
  padding: 60px 40px;
  box-sizing: border-box;
}
</style> -->

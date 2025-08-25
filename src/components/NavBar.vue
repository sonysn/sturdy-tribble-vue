<template>
  <div>
    <!-- Navigation Bar -->
    <nav class="navbar">
      <ul class="nav-list">
        <li><a href="#about" class="nav-link">About</a></li>
        <li><a href="#services" class="nav-link">Services</a></li>
        <li><a href="#contact" class="nav-link">Contacts</a></li>
        <li>
          <a href="#getintouch" class="nav-button">Get in Touch</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script lang="ts" setup>
// no logic needed for now
</script>

<style scoped>
/* Navbar styles */
.navbar {
  width: 100%;
  position: fixed;
  top: 0;
  right: 0;
  padding: 16px;
  background-color: white;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  z-index: 1000;
}

.nav-list {
  display: flex;
  justify-content: flex-end;
  gap: 24px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.nav-link {
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  color: black;
  transition: color 0.3s;
}

.nav-link:hover {
  color: #1a73e8;
}

.nav-button {
  background-color: #1a73e8;
  color: white;
  padding: 20px 16px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  transition: background-color 0.3s;
}

.nav-button:hover {
  background-color: #1557b0;
}

/* Page section styles */
.page-section {
  padding: 100px 20px;
  margin-top: 60px; /* to offset fixed navbar */
  min-height: 100vh;
}
</style>

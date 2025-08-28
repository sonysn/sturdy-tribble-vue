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

<script lang="ts" setup></script>

<style scoped>
.navbar {
  width: 100%;
  position: fixed;
  top: 0;
  right: 0;
  padding: 10px;
  background-color: white;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  display: flex;
  justify-content: end;
  align-items: center;
}

.nav-list {
  display: flex;
  justify-content: flex-end;
  gap: 24px;
  margin: 0;
  padding: 0;
  list-style: none;
  vertical-align: middle;
  justify-content: center;
  align-items: center;
}

.nav-link {
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  color: black;
  transition: color 0.3s;
  background-color: transparent;
}

.nav-link:hover {
  color: #1a73e8;
}

.nav-button {
  background-color: black;
  width: max-content;
  color: white;
  padding: 5px 8px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 500;
  transition: background-color 0.3s;
}

@media only screen and (max-width: 720px) {
  .nav-button {
    font-size: 14px;
    font-weight: 500;
    text-decoration: none;
    color: black;
    transition: color 0.3s;
    background-color: transparent;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px; /* Space between text and icon */
  }

  /* Add the right arrow icon */
  .nav-button::after {
    content: "";
    display: inline-block;
    width: 12px;
    height: 12px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 20 20%22 fill=%22currentColor%22%3E%3Cpath fill-rule=%22evenodd%22 d=%22M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z%22 clip-rule=%22evenodd%22/%3E%3C/svg%3E");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    transform: translateX(4px); /* Space the icon from the text */
  }
}

.nav-button:hover {
  background-color: #1557b0;
}

.page-section {
  padding: 100px 20px;
  margin-top: 60px; /* to offset fixed navbar */
  min-height: 100vh;
}
</style>

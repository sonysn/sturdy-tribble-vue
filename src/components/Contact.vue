<script setup lang="ts">
import { Linkedin, Mail, Twitter } from "lucide-vue-next";
</script>
<template>
  <div :class="$style.contact">
    <h1>Contact</h1>
    <p>
      Connect with Tosin Shokumbi on social media or reach out directly for
      inquiries.
    </p>
    <ul>
      <li>
        <a href="#"><Twitter /> </a>
        <div>Twitter</div>
      </li>
      <li>
        <a href="#"><Linkedin /></a>
        <div>Linkedin</div>
      </li>
      <li>
        <a href="#"><Mail /></a>
        <div>Email</div>
      </li>
    </ul>
  </div>
</template>

<style module>
.contact {
  margin-top: 2rem;
}
.contact p {
  /* text-align: center; */
  margin-left: 15rem;
}
ul {
  display: flex;
  gap: 2rem;
  list-style: none;
  margin-top: 1rem;
}
a {
  color: black;
  text-decoration: none;
  background-color: lightgray;
  padding: 10px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0.5rem;
}
</style>

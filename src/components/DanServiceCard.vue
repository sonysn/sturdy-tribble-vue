<script setup lang="ts">
defineProps<{
  icon: any;
  title: string;
  desc: string;
}>();
</script>

<template>
  <div class="card">
    <component :is="icon" size="32" color="#1a73e8" />
    <h2>{{ title }}</h2>
    <p>{{ desc }}</p>
  </div>
</template>

<style scoped>
.card {
  width: 250px;
  border: 1px solid lightgray;
  border-radius: 10px;
  padding: 15px;
  text-align: center;
  background: #fff;
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.1);
}
.card h2 {
  margin: 0.7rem 0;
  color: #1a73e8;
}
.card p {
  line-height: 1.5;
  color: #444;
}
</style>

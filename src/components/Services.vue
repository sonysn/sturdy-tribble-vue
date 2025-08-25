<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="services">
    <h1 class="title">Services</h1>


    <div class="services-grid">
      <div class="service-card" v-for="(service, i) in services" :key="i">
        <h2>{{ service.title }}</h2>
        <p>{{ service.text }}</p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const services = [
  { title: "Accounting", text: "Comprehensive accounting services for businesses of all sizes." },
  { title: "Digital Skills Training", text: "Training programs to enhance digital literacy and skills." },
  { title: "Business Consulting", text: "Strategic consulting to optimize business operations and growth." },
  { title: "Task Advisory", text: "Expert planning and compliance services." },
  { title: "Public Speaking", text: "Engaging and informative presentations on finance and digital skills." }
]
</script>

<style scoped>
.title {
  font-size: 2.5rem;
  margin-bottom: 15px;
  color: #1a73e8;
  text-align: left;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 30px;
  width: 100%;
}

.service-card {
  background: #f9f9f9;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.service-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
}
.service-card h2 {
  margin-bottom: 10px;
  font-size: 1.3rem;
  color: #1a73e8;
}
.service-card p {
  font-size: 1rem;
  color: #444;
  line-height: 1.6;
}

/* Responsive grid */
@media (max-width: 1200px) {
  .services-grid { grid-template-columns: repeat(3, 1fr); }
}
@media (max-width: 768px) {
  .services-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 480px) {
  .services-grid { grid-template-columns: 1fr; }
}
</style>

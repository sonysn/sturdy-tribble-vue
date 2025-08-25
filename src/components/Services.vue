<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <section id="services">
    <h1 class="title">Services</h1>

    <!-- Flex layout using ServiceCard component -->
    <div class="service-cards">
      <ServiceCard
        v-for="(item, i) in services"
        :key="i"
        :icon="item.icon"
        :title="item.title"
        :desc="item.desc"
      />
    </div>

    <!-- Grid layout -->
    <div class="services-grid">
      <div class="service-card" v-for="(service, i) in services" :key="i">
        <component :is="service.icon" size="32" color="#1a73e8" />
        <h2>{{ service.title }}</h2>
        <p>{{ service.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { BriefcaseBusiness, CircleDollarSign, File, Mic, MonitorPlay } from "lucide-vue-next";
import DanServiceCard from "./DanServiceCard.vue";

const services = [
  {
    icon: CircleDollarSign,
    title: "Accounting",
    desc: "Comprehensive accounting services for businesses of all sizes.",
  },
  {
    icon: MonitorPlay,
    title: "Digital Skills Training",
    desc: "Training programs to enhance digital literacy and skills.",
  },
  {
    icon: BriefcaseBusiness,
    title: "Business Consulting",
    desc: "Strategic consulting to optimize business operations and growth.",
  },
  {
    icon: File,
    title: "Tax Advisory",
    desc: "Expert tax planning and compliance services.",
  },
  {
    icon: Mic,
    title: "Public Speaking",
    desc: "Engaging and informative presentations on finance and digital skills.",
  },
];
</script>

<style scoped>
.title {
  font-size: 2.5rem;
  margin-bottom: 15px;
  color: #1a73e8;
  text-align: left;
}

.service-cards {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 2rem;
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
  text-align: center;
}
.service-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
}
.service-card h2 {
  margin: 10px 0;
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

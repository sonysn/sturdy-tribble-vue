<script setup lang="ts">
import { BriefcaseBusiness, CircleDollarSign, File, Mic, MonitorPlay } from "lucide-vue-next";

const ServiceCardInfo = [
  {
    icon: CircleDollarSign,
    title: "Accounting",
    desc: " Comprehensive accounting services for businesses of all sizes.",
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

<template>
  <div class="services">
    <h1>Services</h1>
    <div class="service-cards">
      <ServiceCard
        v-for="(item, i) in ServiceCardInfo"
        :key="i"
        :icon="item.icon"
        :title="item.title"
        :desc="item.desc"
      />
  </div>
  </div>
</template>

<style>
.service-cards {
  display: flex;
  align-items: center;
  gap: 1rem;
}
.services {
  margin-top: 1rem;
}
</style>

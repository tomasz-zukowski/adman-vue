<script setup>
import jobData from "@/jobs2.json";
import { ref } from "vue";

const jobs = ref(jobData);
console.log(jobs.value);
</script>

<template>
  <section class="bg-green-50 px-4 py-10">
    <div class="container-xl lg:container m-auto">
      <h2 class="text-3xl font-bold text-blue-400 mb-6">
        Browse Jobs
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div v-for="job in jobs" :key="job.id">
          {{ job.title }}
        </div>
      </div>
    </div>
  </section>
</template>

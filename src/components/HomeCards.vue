<script setup>
import { defineProps } from "vue";
import Card from "@/components/Card.vue";

defineProps({
  cards: {
    type: Array,
    default: () => [
      {
        title: "For Developers",
        description: "Browse our Vue jobs and start your career today",
        link: "jobs.html",
        color: "gray",
        bg: "bg-gray-100",
        buttonColor: "black",
      },
      {
        title: "For Employers",
        description: "List your job to find the perfect developer for the role",
        link: "add-job.html",
        color: "green",
        bg: "bg-green-100",
        buttonColor: "green-500",
      },
    ],
  },
})
</script>

<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <Card>
          <h2 class="text-2xl font-bold">For Developers</h2>
          <p class="mt-2 mb-4">
            Browse our Vue jobs and start your career today
          </p>
          <a
            href="jobs.html"
            class="inline-block bg-black text-white rounded-lg px-4 py-2 hover:bg-gray-700"
          >
            Browse Jobs
          </a>
        </Card>
        <Card bg="bg-blue-100">
          <h2 class="text-2xl font-bold">For Employers</h2>
          <p class="mt-2 mb-4">
            List your job to find the perfect developer for the role
          </p>
          <a
            href="add-job.html"
            class="inline-block bg-blue-500 text-white rounded-lg px-4 py-2 hover:bg-blue-600"
          >
            Add Job
          </a>
        </Card>
      </div>
    </div>
  </section>
</template>

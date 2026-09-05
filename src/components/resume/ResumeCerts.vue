<script setup>
import CertificationCard from "./CertificationCard.vue";

const certifications = [
  {
    heading: "Django Essential Training",
    date: "Issued May 2026",
    institution: "LinkedIn Learning",
  },
  {
    heading: "Data and AI Specialist",
    date: "Issued Apr 2026",
    institution: "Cybershujaa",
  },
  {
    heading: "Learning Linux Command Line",
    date: "Issued Mar 2025",
    institution: "LinkedIn Learning",
  },
  {
    heading: "Introduction to Cloud 101",
    date: "Issued Feb 2025",
    institution: "AWS Educate",
  },
  {
    heading: "Version Control",
    date: "Issued Jul 2024",
    institution: "Coursera",
  },
  {
    heading: "Programming with JavaScript",
    date: "Issued Jun 2024",
    institution: "Coursera",
  },
];
</script>

<template>
  <section>
    <h2>Certifications</h2>
    <div>
      <CertificationCard
        v-for="certification in certifications"
        :key="certification.heading"
        v-bind="certification"
      />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../../assets/styles/base.scss";

section {
  h2 {
    @include base.section-heading;
  }

  > div {
    margin: 1rem 0;
  }
}
</style>

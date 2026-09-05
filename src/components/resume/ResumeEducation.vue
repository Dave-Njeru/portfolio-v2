<script setup>
import EducationCard from "./EducationCard.vue";

const educations = [
  {
    title: "Bachelor of Science in Computer Science",
    date: "May 2022 - Dec 2025",
    campus: "Mount Kenya University",
  },
  {
    title: "Diploma in Software Engineering",
    date: "May 2019 - Nov 2021",
    campus: "Zetech University",
  },
];
</script>

<template>
  <section>
    <h2>Education</h2>
    <div>
      <EducationCard
        v-for="education in educations"
        :key="education.title"
        v-bind="education"
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

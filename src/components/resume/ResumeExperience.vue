<script setup>
import ExperienceCard from "./ExperienceCard.vue";

const experiences = [
  {
    title: "Data Specialist",
    date: "Dec 2021 - Present",
    company: "CloudFactory | Hybrid",
    duties: [
      "Process and annotate datasets with 95% accuracy to support ML projects.",
      "Collaborate with cross-functional teams to ensure data quality and consistency.",
      "Conduct data research and entry activities with 98% accuracy.",
      "Utilize data management tools to streamline workflows and improve efficiency.",
    ],
  },
  {
    title: "Quality Assurance",
    date: "Dec 2023 - Aug 2024",
    company: "CloudFactory | Remote",
    duties: [
      "Collaborated with Team Leads on project requirements, expectations, and timelines.",
      "Reviewed 15-member team's output for detects, inconsistencies, and improvements achieving 98% defect-free rate.",
      "Gave constructive feedback and mentorship to resolve challenges.",
      "Partnered with QA team to align standards and ensure project consistency.",
    ],
  },
  {
    title: "Computer Science Student Attachee",
    date: "May 2025 - Aug 2025",
    company: "Esoma Solutions Ltd | On-site",
    duties: [
      "Assisted in the development and testing of software applications, gaining hands-on experience in real-world projects.",
      "Collaborated with team members to learn best practices in coding, debugging, and project management.",
      "Converted word specs to JSON, boosting development pipeline efficiency.",
    ],
  },
];
</script>

<template>
  <section>
    <h2>Experience</h2>
    <div>
      <ExperienceCard
        v-for="experience in experiences"
        :key="experience.title"
        v-bind="experience"
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
    margin-top: 1.5rem;
  }
}
</style>

<script setup>
import SkillsCard from "./SkillsCard.vue";

const skillsData = [
  {
    heading: "Frontend",
    skills: ["HTML5", "CSS3", "JavaScript (ES6+)", "Vue.js"],
  },
  {
    heading: "Backend",
    skills: ["PHP", "Python", "Django", "MySQL"],
  },
  {
    heading: "Tools & Technologies",
    skills: ["Git", "Linux", "AWS"],
  },
  {
    heading: "Data Analysis",
    skills: ["Excel", "SQL", "Power BI", "Tableau"],
  },
];
</script>

<template>
  <section>
    <h2>Skills</h2>
    <div class="skills-container">
      <SkillsCard
        v-for="skill in skillsData"
        :key="skill.heading"
        v-bind="skill"
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

.skills-container {
  display: grid;
  grid-template-columns: repeat(1, minmax(0, 1fr));
  column-gap: 2rem;
  row-gap: 1rem;

  @media (min-width: 640px) {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  @media (min-width: 1024px) {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}
</style>

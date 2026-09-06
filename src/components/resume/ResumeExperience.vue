<script setup>
import ExperienceCard from "./ExperienceCard.vue";

const experiences = [
  {
    title: "Customer Success and Experience Trainee",
    date: "Jun 2026 - Present",
    company: "Smart Applications International Ltd | On-site",
    duties: [
      "Address customer inquiries via phone, chat, and email, providing accurate and timely solutions.",
      "Log customer interactions accurately and escalate complex issues as necessary.",
      "Work collaboratively with team members and other departments to enhance service delivery.",
      "Meet and exceed performance targets, including CSAT, FCR, and adherence metrics.",
    ],
  },
  {
    title: "Data Specialist",
    date: "Dec 2021 - Jun 2026",
    company: "CloudFactory | Hybrid",
    duties: [
      "Processed and annotated datasets with 95% accuracy to support ML projects.",
      "Collaborated with cross-functional teams to ensure data quality and consistency.",
      "Conducted data research and entry activities with 98% accuracy.",
      "Utilized data management tools to streamline workflows and improve efficiency.",
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
    title: "Information Technology Student Attachee",
    date: "Jan 2021 - Apr 2021",
    company: "Rungeto Farmer Cooperative Society | On-site",
    duties: [
      "Troubleshot and maintained the organization’s network infrastructure to ensure reliable connectivity.",
      "Managed, organized, and maintained organizational data to ensure accuracy and accessibility.",
      "Maintained and configured computer systems and other IT equipment to ensure optimal performance.",
      "Provided help desk support by assisting users with technical issues and resolving basic hardware and software problems.",
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

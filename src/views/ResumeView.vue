<script setup>
import AppNavbar from "@/components/shared/AppNavbar.vue";
import AppFooter from "@/components/shared/AppFooter.vue";
import ResumeHeader from "@/components/resume/ResumeHeader.vue";
import ResumeSummary from "@/components/resume/ResumeSummary.vue";
import ResumeExperience from "@/components/resume/ResumeExperience.vue";
import ResumeEducation from "@/components/resume/ResumeEducation.vue";
import ResumeCerts from "@/components/resume/ResumeCerts.vue";
import ResumeSkills from "@/components/resume/ResumeSkills.vue";

</script>

<template>
  <main>
    <AppNavbar />
    <ResumeHeader />
    <ResumeSummary />
    <ResumeExperience />
    <ResumeEducation />
    <ResumeCerts />
    <ResumeSkills />
    <AppFooter />
  </main>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

main {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  border-radius: 0.75rem;
  box-shadow: 0 25px 50px -12px rgb(0, 0, 0, 0.25); // Tailwind's shadow-2xl
  padding: 2rem;
  background-color: rgb(255, 255, 255); // White background

  @media (min-width: 640px) {
    padding: 2.5rem;
  }

  @media (min-width: 768px) {
    padding: 3rem;
  }
}
</style>

<script setup>
import AppNavbar from "@/components/shared/AppNavbar.vue";
import AppFooter from "@/components/shared/AppFooter.vue";
import ProjectsDisplay from "@/components/projects/ProjectsDisplay.vue";
</script>

<template>
  <div>
    <AppNavbar />
    <ProjectsDisplay />
    <AppFooter />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

<script setup>
import Navbar from "@/components/shared/Navbar.vue";
import Footer from "@/components/shared/Footer.vue";
import Projects from "@/components/projects/Projects.vue";
</script>

<template>
  <div>
    <Navbar />
    <Projects />
    <Footer />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

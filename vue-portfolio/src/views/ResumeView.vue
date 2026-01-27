<script setup>
import Navbar from "@/components/shared/Navbar.vue";
import Footer from "@/components/shared/Footer.vue";
import Resume from "@/components/resume/Resume.vue";
</script>

<template>
  <div>
    <Navbar />
    <Resume />
    <Footer />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

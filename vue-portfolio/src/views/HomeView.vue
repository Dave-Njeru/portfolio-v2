<script setup>
import Navbar from "@/components/shared/Navbar.vue";
import Hero from "@/components/home/Hero.vue";
import Footer from "@/components/shared/Footer.vue";
</script>

<template>
  <div>
    <Navbar />
    <Hero />
    <Footer />
  </div>
</template>

<style scoped lang="scss">
div {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>

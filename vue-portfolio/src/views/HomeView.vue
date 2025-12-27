<script setup>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Footer from "@/components/Footer.vue";
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

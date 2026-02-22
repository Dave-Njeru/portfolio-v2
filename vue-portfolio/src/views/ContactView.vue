<script setup>
import Navbar from "@/components/shared/Navbar.vue";
import Footer from "@/components/shared/Footer.vue";
</script>

<template>
  <div>
    <Navbar />
    <div>
        <h2>Contact page coming soon!</h2>
    </div>
    <Footer />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

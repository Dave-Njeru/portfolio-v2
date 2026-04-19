<script setup>
import Navbar from "@/components/shared/Navbar.vue";
import Footer from "@/components/shared/Footer.vue";
import Contact from "@/components/contact/Contact.vue";
</script>

<template>
  <div>
    <Navbar />
    <Contact />
    <Footer />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

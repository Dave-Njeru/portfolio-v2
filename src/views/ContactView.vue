<script setup>
import AppNavbar from "@/components/shared/AppNavbar.vue";
import AppFooter from "@/components/shared/AppFooter.vue";
import ContactForm from "@/components/contact/ContactForm.vue";
</script>

<template>
  <div>
    <AppNavbar />
    <ContactForm />
    <AppFooter />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

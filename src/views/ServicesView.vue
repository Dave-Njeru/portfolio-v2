<script setup>
import AppNavbar from "@/components/shared/AppNavbar.vue";
import AppFooter from "@/components/shared/AppFooter.vue";
import ServicesDisplay from "@/components/services/ServicesDisplay.vue";
</script>

<template>
  <div>
    <AppNavbar />
    <ServicesDisplay />
    <AppFooter />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

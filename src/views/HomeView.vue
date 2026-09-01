<script setup>
import AppNavbar from "@/components/shared/AppNavbar.vue";
import HomeProfile from "@/components/home/HomeProfile.vue";
import AppFooter from "@/components/shared/AppFooter.vue";
</script>

<template>
  <div>
    <AppNavbar />
    <HomeProfile />
    <AppFooter />
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>

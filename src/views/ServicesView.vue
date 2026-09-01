<script setup>
import Navbar from "@/components/shared/Navbar.vue"
import Footer from "@/components/shared/Footer.vue"
import Main from "@/components/services/Main.vue"
</script>

<template>
    <div>
        <Navbar />
        <Main />
        <Footer />
    </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/base.scss";

div {
  @include base.container;
}
</style>
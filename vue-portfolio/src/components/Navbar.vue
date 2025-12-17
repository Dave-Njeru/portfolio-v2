<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <section>
    <header>
      <h2>Dave Ndwiga</h2>

      <nav>
        <RouterLink to="/" class="link">Home</RouterLink>
        <RouterLink to="/services" class="link">Services</RouterLink>
        <RouterLink to="/education" class="link">Education</RouterLink>
        <RouterLink to="/projects" class="link">Projects</RouterLink>
        <RouterLink to="/contact" class="link">Contact</RouterLink>
      </nav>
    </header>
  </section>
</template>

<style scoped lang="scss">
$color: #212529;

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;

  h2 {
    font: {
      weight: 600;
      size: larger;
    }

    color: $color;
  }

  nav {
    display: flex;
    gap: 2rem;

    .link {
      text-decoration: none;
      font-weight: 400;
      color: $color;
      cursor: pointer;

      &:hover {
        color: #0e70ed;
      }
    }
  }
}
</style>

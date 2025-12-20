<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const menuOpen = ref(false);
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>

<template>
  <section>
    <header>
      <h2>Dave Ndwiga</h2>

      <nav :class="{ open: menuOpen }">
        <RouterLink to="/" class="link" @click="menuOpen = false"
          >Home</RouterLink
        >
        <RouterLink to="/services" class="link" @click="menuOpen = false"
          >Services</RouterLink
        >
        <RouterLink to="/education" class="link" @click="menuOpen = false"
          >Education</RouterLink
        >
        <RouterLink to="/projects" class="link" @click="menuOpen = false"
          >Projects</RouterLink
        >
        <RouterLink to="/contact" class="link" @click="menuOpen = false"
          >Contact</RouterLink
        >
      </nav>
      <button class="hamburger" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </button>
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
      size: 1.5rem;
    }

    color: $color;
  }

  nav {
    display: flex;
    gap: 2rem;

    .link {
      text-decoration: none;
      font: {
        weight: 400;
        size: 1rem;
      }
      color: $color;
      cursor: pointer;

      &:hover {
        color: #0e70ed;
      }
    }
  }

  .hamburger {
    display: none;
    flex-direction: column;
    justify-content: center;
    gap: 5px;
    width: 1.5rem;
    height: 1.5rem;
    background: none;
    border: none;
    cursor: pointer;

    span {
      display: block;
      height: 4px;
      width: 100%;
      background: $color;
      border-radius: 2px;
      transition: 0.3s;
    }
  }
}

@media screen and (max-width: 768px) {
  header {
    h2 {
      font: {
        weight: 500;
        size: 1rem;
      }
    }

    nav {
      display: none;
      position: absolute;
      top: 60px;
      left: 0;
      width: 100vw;
      background: #fff;
      flex-direction: column;
      gap: 1.5rem;
      padding: 2rem 1rem 2rem 1rem;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
      z-index: 100;

      .link {
        font: {
          weight: 400;
          size: 1rem;
        }
      }
    }
    nav.open {
      display: flex;
    }
    .hamburger {
      display: flex;
    }
  }
}
</style>

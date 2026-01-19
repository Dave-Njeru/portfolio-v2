<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { RouterLink } from "vue-router";

const menuOpen = ref(false);
// Reference to the header element
const headerRef = ref(null);

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};

const closeMenu = () => {
  menuOpen.value = false;
};

const handleClickOutside = (event) => {
  // Close menu if click is outside navbar
  if (headerRef.value && !headerRef.value.contains(event.target)) {
    closeMenu();
  }
};

const handleScroll = () => {
  // Close menu on scroll
  if (menuOpen.value) {
    closeMenu();
  }
};

// Add event listeners on mount and remove on unmount
onMounted(() => {
  document.addEventListener("click", handleClickOutside);
  window.addEventListener("scroll", handleScroll);
});

// Clean up event listeners
onUnmounted(() => {
  document.removeEventListener("click", handleClickOutside);
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <section>
    <!-- Navbar Component -->
    <header ref="headerRef">
      <!-- Logo / Initials -->
      <div class="logo">
        <span>DN</span>
      </div>
      <!-- Navigation Links -->
      <nav :class="{ open: menuOpen }" class="navigation">
        <RouterLink to="/" class="link" @click="menuOpen = false">Home</RouterLink>
        <RouterLink to="/services" class="link" @click="menuOpen = false">Services</RouterLink>
        <RouterLink to="/education" class="link" @click="menuOpen = false">Education</RouterLink>
        <RouterLink to="/projects" class="link" @click="menuOpen = false">Projects</RouterLink>
        <RouterLink to="/contact" class="link" @click="menuOpen = false">Contact</RouterLink>
      </nav>
      <!-- Hamburger Menu Button -->
      <button @click="toggleMenu" class="menu-button">
        <span class="material-symbols-outlined">menu</span>
      </button>
    </header>
  </section>
</template>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 0;
  white-space: nowrap; // Prevent wrapping of nav links
}

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  color: white;
  background-color: rgb(112, 8, 231); // bg-purple-700 equivalent

  span {
    font: {
      weight: 700;
      size: 1.25rem;
    }
  }
}

.navigation {
  display: none;
  align-items: center;
  gap: 2rem;

  &.open {
    display: flex; // Show menu when open
    flex-direction: column; // Stack links vertically
    position: absolute; // Position over content
    top: 4.5rem; // Below the header
    right: 1rem; // Align to the right
    background-color: white;
    padding: 1rem 2rem;
    border: 1px solid rgb(229, 231, 235);
    border-radius: 0.5rem;
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
      0 4px 6px -2px rgba(0, 0, 0, 0.05); // shadow-lg equivalent
    z-index: 10; // Ensure it appears above other content
  }

  @media (min-width: 769px) {
    display: flex; // Always show menu on larger screens
    position: static; // Reset position
    flex-direction: row;
    box-shadow: none;
    border: none;
    padding: 0;
  }

  .link {
    font: {
      weight: 500;
      size: 1rem;
    }

    text-decoration: none;
    color: rgb(33, 37, 41);
    cursor: pointer;
    transition: all 0.1s ease-in;

    &:hover {
      color: rgb(37, 99, 235);
    }
  }
}

.menu-button {
  background: none;
  border: none;
  cursor: pointer;

  span {
    font-size: 1.875rem;
    line-height: 2.25rem;
    color: rgb(33, 37, 41);
  }

  @media (min-width: 769px) {
    display: none;
  }
}
</style>
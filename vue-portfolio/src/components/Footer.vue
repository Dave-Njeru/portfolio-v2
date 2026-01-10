<script setup>
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer>
    <p>&copy; {{ currentYear }} My Portfolio. All rights reserved.</p>
  </footer>
</template>

<style scoped lang="scss">
footer {
  margin-top: auto;
  padding: 4rem 0 1rem 0;
  text-align: center;
  font-size: 0.875rem;
}
</style>

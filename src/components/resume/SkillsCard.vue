<script setup>
defineProps({
  heading: {
    type: String,
    required: true,
  },
  skills: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="skills-item">
    <h4>{{ heading }}</h4>
    <ul>
      <li v-for="skill in skills" :key="skill">
        {{ skill }}
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.skills-item {
  h4 {
    font: {
      size: 1rem;
      weight: 700;
    }

    line-height: 1.5rem;
    color: rgb(33, 33, 33);
  }

  ul {
    margin: 0.5rem 0 0 1.25rem;
    list-style-type: disc;
    list-style-position: outside;
    color: #4b5563;
  }
}
</style>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  date: {
    type: String,
    required: true,
  },
  company: {
    type: String,
    required: true,
  },
  duties: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <article class="experience-card">
    <div class="experience-header">
      <h3>{{ title }}</h3>
      <p>{{ date }}</p>
    </div>
    <p class="company">{{ company }}</p>
    <ul class="job-duties">
      <li v-for="duty in duties" :key="duty">{{ duty }}</li>
    </ul>
  </article>
</template>

<style scoped lang="scss">
.experience-card {
  margin-top: 1.5rem;
}

.experience-header {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  gap: 1rem;

  h3 {
    font: {
      size: 1.125rem;
      weight: 700;
    }

    line-height: 1.75rem;
    color: rgb(33, 33, 33);
  }

  p {
    flex-shrink: 0;
    font: {
      size: 0.875rem;
      weight: 500;
    }

    color: #4b5563;
  }
}

.company {
  font: {
    size: 1rem;
    weight: 500;
  }

  line-height: 1.5rem;
  color: #135bec;
}

.job-duties {
  margin: 0.25rem 0;
  padding-left: 1.25rem;
  list-style-type: disc;
  list-style-position: outside;
  font-size: 1rem;
  line-height: 1.625;
  color: #4b5563;
}
</style>

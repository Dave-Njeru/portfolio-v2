<script setup>
defineProps({
  heading: {
    type: String,
    required: true,
  },
  description: {
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
  <div class="service-card">
    <span class="material-symbols-outlined service-icon">code</span>
    <div class="card-content">
      <h2>{{ heading }}</h2>
      <p>
        {{ description }}
      </p>
    </div>
    <div class="card-skills">
      <span v-for="skill in skills" :key="skill">
        {{ skill }}
      </span>
    </div>
  </div>
</template>

<style scoped lang="scss">
.service-card {
  display: flex;
  flex: 1 1 0%;
  flex-direction: column;
  gap: 1rem;
  padding: 1.5rem;
  border: 1px solid rgb(226, 232, 240);
  border-radius: 0.75rem;
  box-shadow: 0 1px 2px rgb(0 0 0 / 0.05);
  background-color: rgb(255, 255, 255);
  transition: all 300ms ease-in-out;

  &:hover {
    box-shadow: 0 4px 6px rgb(0 0 0 / 0.1);
  }
}

.service-icon {
  font-size: 1.875rem;
  color: rgb(59, 130, 246);
}

.card-content {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;

  h2 {
    font: {
      size: 1.25rem;
      weight: 700;
    }

    color: rgb(15, 23, 42);
    line-height: 1.25;
  }

  p {
    font: {
      size: 1rem;
      weight: 400;
    }

    color: rgb(100, 116, 139);
    line-height: 1.5;
  }
}

.card-skills {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  padding-top: 0.5rem;

  span {
    background-color: rgb(239, 246, 255);
    color: rgb(37, 99, 235);

    font: {
      size: 0.875rem;
      weight: 500;
    }

    padding: 0.25rem 0.75rem;
    border-radius: 0.375rem;
    line-height: 1;
  }
}
</style>

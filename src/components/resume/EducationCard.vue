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
  campus: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <article>
    <div class="education-item">
      <div>
        <span class="material-symbols-outlined">school</span>
        <h3>{{ title }}</h3>
      </div>
      <p>{{ date }}</p>
    </div>
    <p class="campus">{{ campus }}</p>
  </article>
</template>

<style scoped lang="scss">
.education-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;

  div {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    span {
      font-size: 1.25rem;
      line-height: 1.75rem;
      color: #4b5563;
    }

    h3 {
      font: {
        size: 1.125rem;
        weight: 700;
      }

      line-height: 1.75rem;
      color: #212121;
    }
  }

  p {
    font: {
      size: 0.875rem;
      weight: 500;
    }

    line-height: 1.25rem;
    color: #4b5563;
  }
}

.campus {
  font: {
    size: 1rem;
    weight: 500;
  }

  line-height: 1.5rem;
  padding-left: 1.75rem;
  color: #135bec;
}
</style>

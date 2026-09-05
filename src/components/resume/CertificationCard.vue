<script setup>
defineProps({
  heading: {
    type: String,
    required: true,
  },
  date: {
    type: String,
    required: true,
  },
  institution: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div>
    <div class="cert-item-header">
      <div>
        <span class="material-symbols-outlined">verified_user</span>
        <h3>{{ heading }}</h3>
      </div>
      <p>{{ date }}</p>
    </div>
    <p class="institution">{{ institution }}</p>
  </div>
</template>

<style scoped lang="scss">
.cert-item-header {
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

.institution {
  font: {
    size: 1rem;
    weight: 500;
  }

  line-height: 1.5rem;
  color: #135bec;
  padding-left: 1.75rem;
}
</style>

<script setup>
import ServiceCard from "./ServiceCard.vue";

const services = [
  {
    heading: "Web Development",
    description:
      "Building responsive and dynamic websites using the latest technologies like Vue.js and Django.",
    skills: ["HTML", "CSS", "JavaScript", "Vue.js", "Django", "SQL"],
  },
  {
    heading: "IT Support",
    description:
      "Offering reliable IT support services including troubleshooting, maintenance, and network management.",
    skills: ["Network Setup", "Troubleshooting", "Maintenance", "Security"],
  },
  {
    heading: "Database Management",
    description:
      "Designing and maintaining efficient database systems to ensure data integrity and performance.",
    skills: ["SQL", "Data Modeling", "Backup & Recovery"],
  },
];
</script>

<template>
  <main>
    <!-- Heading Section -->
    <div class="page-title">
      <h1>My Skills &amp; Services</h1>
    </div>
    <!-- Summary Section -->
    <div>
      <p class="page-summary">
        I specialize in creating robust web applications, providing
        comprehensive IT support, and managing complex database systems to help
        businesses succeed.
      </p>
    </div>
    <!-- Services Section -->
    <div class="services-container">
      <ServiceCard
        v-for="service in services"
        :key="service.heading"
        v-bind="service"
      />
    </div>
    <!-- CTA Button -->
    <div class="cta-container">
      <router-link to="/contact" class="cta-button"
        ><span>Let's Work Together</span></router-link
      >
    </div>
  </main>
</template>

<style scoped lang="scss">
main {
  padding: {
    top: 3rem;
    bottom: 4rem;
  }
}

.page-title {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 0.75rem;
  padding: 1rem;

  h1 {
    font: {
      size: 2.25rem;
      weight: 900;
    }

    letter-spacing: -0.033em;
    line-height: 2.5rem;
    color: rgb(15, 23, 42);
  }
}

.page-summary {
  font: {
    size: 1rem;
    weight: 400;
  }

  line-height: 1.5;
  color: rgb(71, 85, 105);
  padding: 2rem 1rem;
}

.services-container {
  display: grid;
  grid-template-columns: minmax(0, 1fr);
  gap: 1.5rem;
  padding: 1rem;

  @media (min-width: 768px) {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  @media (min-width: 1024px) {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}

.cta-container {
  display: flex;
  justify-content: center;
  padding: 3rem 1rem;

  .cta-button {
    display: flex;
    align-items: center; // Centers the span text vertically
    justify-content: center; // Centers the span text horizontally
    min-width: 5.25rem;
    max-width: 30rem;
    background-color: rgb(59, 130, 246);
    color: rgb(255, 255, 255);
    text-decoration: none; // Removes underline from router-link

    font: {
      size: 1rem;
      weight: 600;
    }

    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 0.5rem;
    cursor: pointer;
    transition: background-color 300ms ease-in-out;

    &:hover {
      background-color: rgb(37, 99, 235);
    }

    span {
      overflow: hidden; // Hides overflowed text
      text-overflow: ellipsis; // Adds ellipsis for overflowed text ("...")
      white-space: nowrap; // Prevents text from wrapping to the next line
    }
  }
}
</style>

<script setup>
import Header from './Header.vue';
import Summary from './Summary.vue';
import Experience from './Experience.vue';
import Education from './Education.vue';
import Certs from './Certs.vue';
import Skills from './Skills.vue';
</script>

<template>
    <main>
        <!-- Header -->
        <Header />
        <!-- Summary Section -->
        <Summary />
        <!-- Experience Section -->
        <Experience />
        <!-- Education Section -->
        <Education />
        <!-- Certifications Section -->
        <Certs />
        <!-- Skills Section -->
        <Skills />
    </main>
</template>

<style scoped lang="scss">
main {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    border-radius: 0.75rem;
    box-shadow: 0 25px 50px -12px rgb(0, 0, 0, 0.25); // Tailwind's shadow-2xl
    padding: 2rem;
    background-color: rgb(255, 255, 255); // White background

    @media (min-width: 640px) {
        padding: 2.5rem;
    }

    @media (min-width: 768px) {
        padding: 3rem;
    }
}
</style>
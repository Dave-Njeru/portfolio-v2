<template>
  <section>
    <h2>Summary</h2>
    <p>
      I am a recent computer science graduate who excels at developing robust
      web applications while actively building expertise in data and AI to
      create intelligent systems that solve real-world challenges. My strong
      problem-solving, analytical thinking, and time management skills enable me
      to deliver efficient and innovative solutions. I'm eager to apply my
      academic knowledge in dynamic opportunities where I can contribute and
      further my growth.
    </p>
  </section>
</template>

<style scoped lang="scss">
@use "../../assets/styles/base.scss";

section {
  h2 {
    @include base.section-heading;
  }

  p {
    font: {
      size: 1rem;
      weight: 400;
    }

    line-height: 1.625;
    color: rgb(75, 85, 99);
  }
}
</style>

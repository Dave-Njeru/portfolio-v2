<template>
  <section>
    <h2>Education</h2>
    <div>
      <!-- Education Item 1-->
      <div>
        <div class="education-item">
          <div>
            <span class="material-symbols-outlined">school</span>
            <h3>Bachelor of Science in Computer Science</h3>
          </div>
          <p>May 2022 - Dec 2025</p>
        </div>
        <p class="campus">Mount Kenya University</p>
      </div>
      <!-- Education Item 2-->
      <div>
        <div class="education-item">
          <div>
            <span class="material-symbols-outlined">school</span>
            <h3>Diploma in Software Engineering</h3>
          </div>
          <p>May 2019 - Nov 2021</p>
        </div>
        <p class="campus">Zetech University</p>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../../assets/styles/base.scss";

section {
  h2 {
    @include base.section-heading;
  }

  > div {
    margin: 1rem 0;
  }
}

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

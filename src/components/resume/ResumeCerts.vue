<template>
  <section>
    <h2>Certifications</h2>
    <div>
      <!-- Certification Item 1-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Data and AI Specialist</h3>
          </div>
          <p>Ongoing</p>
        </div>
        <p class="institution">Cybershujaa</p>
      </div>
      <!-- Certification Item 2-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Information Technology Fundamentals (IT Support)</h3>
          </div>
          <p>Ongoing</p>
        </div>
        <p class="institution">IBM SkillsBuild</p>
      </div>
      <!-- Certification Item 3-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Learning Linux Command Line</h3>
          </div>
          <p>Issued Mar 2025</p>
        </div>
        <p class="institution">LinkedIn Learning</p>
      </div>
      <!-- Certification Item 4-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Introduction to Cloud 101</h3>
          </div>
          <p>Issued Feb 2025</p>
        </div>
        <p class="institution">AWS Educate</p>
      </div>
      <!-- Certification Item 5-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Version Control</h3>
          </div>
          <p>Issued Jul 2024</p>
        </div>
        <p class="institution">Coursera</p>
      </div>
      <!-- Certification Item 6-->
      <div>
        <div class="cert-item-header">
          <div>
            <span class="material-symbols-outlined">verified_user</span>
            <h3>Programming with JavaScript</h3>
          </div>
          <p>Issued Jun 2024</p>
        </div>
        <p class="institution">Coursera</p>
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

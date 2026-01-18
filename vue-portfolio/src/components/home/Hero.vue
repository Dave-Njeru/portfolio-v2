<template>
  <main>
    <!-- Hero Section -->
    <div class="hero-container">
      <div class="hero-text">
        <!-- Text Content -->
        <div class="text-content">
          <h1>Dave Ndwiga - ICT Specialist</h1>
          <h2>
            I am a recent computer science graduate passionate about designing and
            building applications, collaborating with teams to solve complex
            problems, and delivering user-friendly solutions that meet clients'
            needs. I offer services in web development, technical support, and
            database administration. I seek opportunities to apply my academic
            training, contribute to innovative projects, and provide valuable
            expertise to your team.
          </h2>
        </div>
        <!-- CTA Buttons -->
        <div class="button-group">
          <button><span>Explore My Projects</span></button>
          <button><span>Download Resume</span></button>
        </div>
      </div>
      <!-- Profile Image -->
      <div class="profile-image">
        <img src="@/assets/images/profile.jpg" alt="professional headshot of Dave Ndwiga" />
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
main {
  padding: 4rem 0;

  @media (min-width: 640px) {
    padding: 6rem 0;
  }

  @media (min-width: 1024px) {
    padding: 8rem 0;
  }
}

.hero-container {
  display: grid;
  grid-template-columns: 1fr;
  gap: 3rem;
  align-items: center;

  @media (min-width: 1024px) {
    grid-template-columns: repeat(2, 1fr);
    gap: 6rem;
  }
}

.hero-text {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.text-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-align: center;

  @media (min-width: 1024px) {
    text-align: left;
  }

  h1 {
    font-size: 2.25rem;
    font-weight: 900;
    color: rgb(33, 37, 41);
    line-height: 1.25;
    letter-spacing: -0.05em;

    @media (min-width: 640px) {
      font-size: 3rem;
    }

    @media (min-width: 1024px) {
      font-size: 3.75rem;
    }
  }

  h2 {
    font-size: 1rem;
    font-weight: 400;
    color: rgb(75, 85, 99);
    line-height: 1.5;

    @media (min-width: 640px) {
      font-size: 1.25rem;
      line-height: 1.75;
    }
  }
}

.button-group {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;

  @media (min-width: 640px) {
    flex-direction: row;
    justify-content: center;
  }

  @media (min-width: 1024px) {
    justify-content: flex-start;
  }

  button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    min-width: 5.25rem;
    max-width: 30rem;
    overflow: hidden;
    border: none;
    border-radius: 0.5rem;
    height: 3rem;
    padding: 0 1.5rem;

    font: {
      size: 1rem;
      weight: 700;
    }

    line-height: 1.5;
    letter-spacing: 0.015em;
    background-color: rgb(37, 99, 235);
    color: white;
    cursor: pointer;
    transition: all 0.3s ease;

    span {
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
    }

    &:hover {
      opacity: 0.9;
    }

    @media (min-width: 640px) {
      width: auto;
    }
  }
}

.profile-image {
  display: flex;
  justify-content: center;

  img {
    width: 20rem;
    height: 20rem;
    border-radius: 50%;
    object-fit: cover;

    @media (min-width: 640px) {
      width: 24rem;
      height: 24rem;
    }
  }
}
</style>
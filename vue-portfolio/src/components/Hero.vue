<template>
  <main>
    <div id="description">
      <h1>Dave Ndwiga - IT Specialist</h1>
      <h2>
        I am a recent computer science graduate passionate about designing and
        building applications, collaborating with teams to solve complex
        problems, and delivering user-friendly solutions that meet clients'
        needs. I offer services in web development, technical support, and
        database administration. I seek opportunities to apply my academic
        training, contribute to innovative projects, and provide valuable
        expertise to your team.
      </h2>
      <div>
        <button><a href="#">Explore My Projects</a></button>
        <button><a href="#">Download Resume</a></button>
      </div>
    </div>

    <div id="hero-image">
      <img src="@/assets/images/profile.jpg" alt="Hero Image" />
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "@/assets/styles/variables.scss";
main {
  display: grid;
  grid-template-columns: repeat(2, 1fr);

  div#description {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 2rem;

    h1 {
      font: {
        weight: 900;
        size: 3.75rem;
      }
      //   letter-spacing: -0.05rem;
      //   line-height: 1.25rem;
      color: variables.$color;
    }

    h2 {
      font-size: 1.2rem;
      margin-bottom: 2rem;
      // line-height: 1.5;
    }

    div {
      display: flex;
      gap: 1rem;

      button {
        padding: 0.75rem 1.5rem;
        font-size: 1rem;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        background-color: #007bff;
        color: white;

        a {
          text-decoration: none;
          color: white;
        }
      }
    }
  }

  div#hero-image {
    width: 25rem;
    height: 25rem;
    margin: auto;

    img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      object-fit: cover;
    }
  }
}

@media screen and (max-width: 768px) {
  main {
    grid-template-columns: 1fr;
    text-align: center;

    div#description {
      h1 {
        font-size: 2.5rem;
      }

      h2 {
        font-size: 1rem;
      }

      div {
        flex-direction: column;
        align-items: center;
      }
    }

    div#hero-image {
      width: 15rem;
      height: 15rem;
      margin: 2rem auto 2rem auto;
    }
  }
}
</style>

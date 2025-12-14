<template>
  <section>
    <header>
      <h2>Dave Ndwiga</h2>

      <nav>
        <ul>
          <li>Home</li>
          <li>Services</li>
          <li>Education</li>
          <li>Projects</li>
          <li>Contact</li>
        </ul>
      </nav>
    </header>
  </section>
</template>

<style scoped lang="scss">
$color: #212529;

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;

  h2 {
    font: {
      weight: 600;
      size: larger;
    }

    color: $color;
  }

  nav {
    ul {
      display: flex;
      gap: 2rem;

      li {
        list-style-type: none;
        font-weight: 400;
        cursor: pointer;
        color: $color;

        &:hover {
          color: #0e70ed;
        }
      }
    }
  }
}
</style>

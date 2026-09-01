<template>
  <header>
    <h1>Dave Ndwiga</h1>
    <p>ICT Specialist</p>
    <div class="contact-info">
      <div>
        <svg aria-hidden="true" fill="currentColor" viewBox="0 0 24 24">
          <path
            clip-rule="evenodd"
            d="M19.5 0h-15A4.5 4.5 0 000 4.5v15A4.5 4.5 0 004.5 24h15a4.5 4.5 0 004.5-4.5v-15A4.5 4.5 0 0019.5 0zm-11.25 19.5h-3V9h3v10.5zm-1.5-12a1.875 1.875 0 110-3.75 1.875 1.875 0 010 3.75zM19.5 19.5h-3v-5.25c0-1.25-.025-2.85-1.75-2.85-1.75 0-2.025 1.375-2.025 2.75V19.5h-3V9h2.875v1.313h.038c.387-.75 1.337-1.538 2.837-1.538 3.025 0 3.588 2 3.588 4.5v5.225z"
            fill-rule="evenodd"
          ></path>
        </svg>
        <a href="https://www.linkedin.com/in/ndwigadave/" target="_blank"
          >in/ndwigadave</a
        >
      </div>
      <div>
        <svg aria-hidden="true" fill="currentColor" viewBox="0 0 24 24">
          <path
            clip-rule="evenodd"
            d="M12 2C6.477 2 2 6.477 2 12c0 4.286 2.89 7.92 6.837 9.163.498.09.68-.216.68-.48 0-.236-.008-.864-.013-1.695-2.804.604-3.396-1.35-3.396-1.35-.452-1.15-1.104-1.455-1.104-1.455-.903-.618.068-.605.068-.605 1.0.07 1.527 1.025 1.527 1.025.888 1.523 2.327 1.083 2.895.828.09-.643.348-1.083.633-1.33-2.21-.25-4.533-1.102-4.533-4.924 0-1.087.39-1.978 1.028-2.675-.104-.253-.446-1.267.098-2.638 0 0 .837-.268 2.742 1.022A9.63 9.63 0 0112 6.82c.85.004 1.705.114 2.504.336 1.905-1.29 2.74-1.022 2.74-1.022.546 1.37.202 2.385.1 2.638.64.697 1.026 1.588 1.026 2.675 0 3.833-2.327 4.67-4.542 4.914.357.308.678.918.678 1.85 0 1.335-.012 2.415-.012 2.742 0 .267.18.577.688.48A10.007 10.007 0 0022 12c0-5.523-4.477-10-10-10z"
            fill-rule="evenodd"
          ></path>
        </svg>
        <a href="https://github.com/Dave-Njeru" target="_blank"
          >github/Dave-Njeru</a
        >
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  border-bottom-style: solid;
  border-bottom-width: 1px;
  border-color: rgb(229, 231, 235);
  padding-bottom: 2rem;

  h1 {
    font: {
      size: 2.25rem;
      weight: 700;
    }

    color: rgb(33, 33, 33);
    line-height: 1.25;
    text-align: left;
    letter-spacing: -0.025em;

    @media (min-width: 768px) {
      font-size: 3rem;
      line-height: 1;
    }
  }

  p {
    font: {
      size: 1.25rem;
      weight: 500;
    }

    color: rgb(19, 91, 236);
    padding-top: 0.5rem;
    line-height: 1.5;
  }
}

.contact-info {
  margin-top: 1.5rem;
  display: flex;
  flex-wrap: wrap;
  column-gap: 1.5rem;
  row-gap: 0.75rem;
  font-size: 0.875rem;
  line-height: 1.25rem;
}

.contact-info div {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: rgb(75, 85, 99);

  span {
    font-size: 1.125rem;
    line-height: 1.75rem;
  }

  a {
    color: inherit;
    text-decoration: none;
    transition: color 0.3s ease;

    &:hover {
      color: rgb(19, 91, 236);
    }
  }

  svg {
    width: 1.5em;
    height: 1.5rem;
  }
}
</style>

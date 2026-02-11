<template>
    <header>
        <h1>Dave Ndwiga</h1>
        <p>ICT Specialist</p>
        <div class="contact-info">
            <div>
                <span class="material-symbols-outlined">mail</span>
                <a href="mailto:davenjeru9@gmail.com">davenjeru9@gmail.com</a>
            </div>
            <div>
                <span class="material-symbols-outlined">phone</span>
                <a href="tel:+254111376951">+254 111376951</a>
            </div>
            <div>
                <svg aria-hidden="true" fill="currentColor" viewBox="0 0 24 24">
                    <path clip-rule="evenodd"
                        d="M19.5 0h-15A4.5 4.5 0 000 4.5v15A4.5 4.5 0 004.5 24h15a4.5 4.5 0 004.5-4.5v-15A4.5 4.5 0 0019.5 0zm-11.25 19.5h-3V9h3v10.5zm-1.5-12a1.875 1.875 0 110-3.75 1.875 1.875 0 010 3.75zM19.5 19.5h-3v-5.25c0-1.25-.025-2.85-1.75-2.85-1.75 0-2.025 1.375-2.025 2.75V19.5h-3V9h2.875v1.313h.038c.387-.75 1.337-1.538 2.837-1.538 3.025 0 3.588 2 3.588 4.5v5.225z"
                        fill-rule="evenodd"></path>
                </svg>
                <a href="https://www.linkedin.com/in/ndwigadave/" target="_blank">in/ndwigadave</a>
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
        width: 1rem;
        height: 1rem;
    }
}
</style>
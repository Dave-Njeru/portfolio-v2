<template>
    <section>
        <h2>Skills</h2>
        <div class="skills-container">
            <!-- Skill Item 1-->
            <div class="skills-item">
                <h4>Frontend</h4>
                <ul>
                    <li>HTML5</li>
                    <li>CSS3</li>
                    <li>JavaScript (ES6+)</li>
                    <li>Vue.js</li>
                </ul>
            </div>
            <!-- Skill Item 2-->
            <div class="skills-item">
                <h4>Backend</h4>
                <ul>
                    <li>PHP</li>
                    <li>Python</li>
                    <li>Django</li>
                    <li>MySQL</li>
                </ul>
            </div>
            <!-- Skill Item 3-->
            <div class="skills-item">
                <h4>Tools & Technologies</h4>
                <ul>
                    <li>Git</li>
                    <li>Linux</li>
                    <li>AWS</li>
                </ul>
            </div>
            <!-- Skill Item 4-->
            <div class="skills-item">
                <h4>Data Analysis</h4>
                <ul>
                    <li>Excel</li>
                    <li>SQL</li>
                    <li>Power BI</li>
                    <li>Tableau</li>
                </ul>
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

    >div {
        margin-top: 1.5rem;
    }
}

.skills-container {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    column-gap: 2rem;
    row-gap: 1rem;

    @media (min-width: 640px) {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    @media (min-width: 1024px) {
        grid-template-columns: repeat(4, minmax(0, 1fr));
    }
}

.skills-item {
    h4 {
        font: {
            size: 1rem;
            weight: 700;
        }

        line-height: 1.5rem;
        color: rgb(33, 33, 33);
    }

    ul {
        margin: 0.5rem 0 0 1.25rem;
        list-style-type: disc;
        list-style-position: outside;
        color: #4b5563;
    }
}
</style>
<template>
    <main>
        <!-- Page Heading -->
        <div class="page-header">
            <div class="page-header__content"> <!-- BEM naming convention-->
                <h2>Experience &amp; Education</h2>
                <p>A timeline of my professional and academic journey</p>
            </div>
        </div>
        <!-- Professional Experience Section -->
        <section class="experience-section">
            <!-- Section Heading -->
            <h2>Professional Experience</h2>
            <!-- Experience Entries -->
            <div class="experience-entries">
                <!-- Item 1 -->
                <div class="experience">
                    <span class="material-symbols-outlined">work</span>
                    <div></div>
                </div>
                <div class="experience-info">
                    <p>Data Specialist</p>
                    <p>CloudFactory | Dec 2021 - Present | Remote</p>
                </div>
                <!-- Item 2 -->
                <div class="experience">
                    <span class="material-symbols-outlined">work</span>
                    <div></div>
                </div>
                <div class="experience-info">
                    <p>Quality Assurance</p>
                    <p>CloudFactory | Dec 2023 - Aug 2024 | Remote</p>
                </div>
                <!-- Item 3 -->
                <div class="experience">
                    <span class="material-symbols-outlined">work</span>
                </div>
                <div class="experience-info">
                    <p>Computer Science Student Attachee</p>
                    <p>Esoma Solutions Ltd | May 2025 - Aug 2025 | On-site</p>
                </div>
            </div>
        </section>
        <!-- Education Section -->
        <section class="education-section">
            <!-- Section Heading -->
            <h2>Education</h2>
            <!-- Education Entries -->
            <div class="education-entries">
                <!-- Item 1 -->
                <div class="education">
                    <span class="material-symbols-outlined">school</span>
                    <div></div>
                </div>
                <div class="education-info">
                    <p>Data &amp; AI Specialist Program</p>
                    <p>Cyber Shujaa | Ongoing</p>
                </div>
                <!-- Item 2 -->
                <div class="education">
                    <span class="material-symbols-outlined">school</span>
                    <div></div>
                </div>
                <div class="education-info">
                    <p>Bachelor of Science in Computer Science</p>
                    <p>Mount Kenya University | Graduated Dec 2025</p>
                </div>
                <!-- Item 3 -->
                <div class="education">
                    <span class="material-symbols-outlined">school</span>
                </div>
                <div class="education-info">
                    <p>Diploma in Software Engineering</p>
                    <p>Zetech University | Graduated Nov 2021</p>
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped lang="scss">
main {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    padding: 2.5rem 0;

    @media (min-width: 640px) {
        padding: 3rem 0;
    }

    @media (min-width: 768px) {
        padding: 4rem 0;
    }
}

.page-header {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 2.5rem;
    // padding: 0 2.5rem;

    &__content {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;

        h2 {
            font: {
                size: 2.25rem;
                weight: 900;
            }

            line-height: 1.25;
            letter-spacing: -0.033em;
        }

        p {
            font: {
                size: 1rem;
                weight: 400;
            }

            line-height: 1.5;
            color: rgb(75, 85, 99);
        }
    }
}

.experience-section {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;

    h2 {
        font: {
            size: 1.375rem;
            weight: 800;
        }

        // padding: 0 1rem;
        line-height: 1.25;
        letter-spacing: -0.015em;
    }
}

.experience-entries {
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 1rem;
}

.experience {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.25rem;
    padding-top: 0.75rem;

    span {
        font-size: 1.5rem;
        line-height: 2rem;
        color: rgb(75, 85, 99);
    }

    div {
        width: 2px;
        flex-grow: 1;
        background-color: rgb(229, 231, 235);
    }
}

.experience-info {
    display: flex;
    flex: 1 1 0%; // Allow to grow and shrink
    flex-direction: column;
    padding: 0.75rem 0;

    p:first-of-type {
        font: {
            size: 1rem;
            weight: 500;
        }

        line-height: 1.5;
        color: rgb(0, 0, 0);
    }

    p:last-of-type {
        font: {
            size: 1rem;
            weight: 400;
        }

        line-height: 1.25;
        color: rgb(75, 85, 99);
    }
}

.education-section {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;

    h2 {
        font: {
            size: 1.375rem;
            weight: 700;
        }

        // padding: 0 1rem;
        line-height: 1.25;
        letter-spacing: -0.015em;
        color: rgb(0, 0, 0);
    }
}

.education-entries {
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 1rem;
}

.education {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.25rem;
    padding-top: 0.75rem;

    span {
        font-size: 1.5rem;
        line-height: 2rem;
        color: rgb(75, 85, 99);
    }

    div {
        width: 2px;
        flex-grow: 1;
        background-color: rgb(229, 231, 235);
    }
}

.education-info {
    display: flex;
    flex: 1 1 0%; // Allow to grow and shrink
    flex-direction: column;
    padding: 0.75rem 0;

    p:first-of-type {
        font: {
            size: 1rem;
            weight: 500;
        }

        line-height: 1.5;
        color: rgb(0, 0, 0);
    }

    p:last-of-type {
        font: {
            size: 1rem;
            weight: 400;
        }

        line-height: 1.25;
        color: rgb(75, 85, 99);
    }
}
</style>
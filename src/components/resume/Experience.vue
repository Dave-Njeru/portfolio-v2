<template>
    <section>
        <h2>Experience</h2>
        <div>
            <!-- Experience Item 1-->
            <div>
                <div class="experience-header">
                    <h3>Data Specialist</h3>
                    <p>Dec 2021 - Present</p>
                </div>
                <p class="company">CloudFactory | Hybrid</p>
                <ul class="job-duties">
                    <li>Process and annotate datasets with 95% accuracy to support ML projects.</li>
                    <li>Collaborate with cross-functional teams to ensure data quality and consistency.</li>
                    <li>Conduct data research and entry activities with 98% accuracy.</li>
                    <li>Utilize data management tools to streamline workflows and improve efficiency.</li>
                </ul>
            </div>
            <!-- Experience Item 2-->
            <div>
                <div class="experience-header">
                    <h3>Quality Assurance</h3>
                    <p>Dec 2023 - Aug 2024</p>
                </div>
                <p class="company">CloudFactory | Remote</p>
                <ul class="job-duties">
                    <li>Collaborated with Team Leads on project requirements, expectations, and timelines.</li>
                    <li>Reviewed 15-member team's output for detects, inconsistencies, and improvements achieving 98%
                        defect-free rate.</li>
                    <li>Gave constructive feedback and mentorship to resolve challenges.</li>
                    <li>Partnered with QA team to align standards and ensure project consistency.</li>
                </ul>
            </div>
            <!-- Experience Item 3-->
            <div>
                <div class="experience-header">
                    <h3>Computer Science Student Attachee</h3>
                    <p>May 2025 - Aug 2025</p>
                </div>
                <p class="company">Esoma Solutions Ltd | On-site</p>
                <ul class="job-duties">
                    <li>Assisted in the development and testing of software applications, gaining hands-on
                        experience in real-world projects.
                    </li>
                    <li>Collaborated with team members to learn best practices in coding, debugging, and project
                        management.
                    </li>
                    <li>Converted word specs to JSON, boosting development pipeline efficiency.</li>
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

.experience-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;

    h3 {
        font: {
            size: 1.125rem;
            weight: 700;
        }

        line-height: 1.75rem;
        color: rgb(33, 33, 33);
    }

    p {
        font: {
            size: 0.875rem;
            weight: 500;
        }

        color: #4b5563;
    }
}

.company {
    font: {
        size: 1rem;
        weight: 500;
    }

    line-height: 1.5rem;
    color: #135bec;
}

.job-duties {
    margin: 0.25rem 0 0.25rem 1.25rem;
    list-style-type: disc;
    list-style-position: outside;
    font-size: 1rem;
    line-height: 1.625;
    color: #4b5563;
}
</style>
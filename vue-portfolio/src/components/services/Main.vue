<template>
    <main>
        <!-- Heading Section -->
        <div>
            <h1 class="page-title">My Skills &amp; Services</h1>
        </div>
        <!-- Summary Section -->
        <div>
            <p class="page-summary">
                I specialize in creating robust web applications,
                providing comprehensive IT support, and managing complex
                database systems to help businesses succeed.
            </p>
        </div>
        <!-- Services Section -->
        <div class="services-container">
            <!-- Service Card 1: Web Development-->
            <div class="service-card">
                <span class="material-symbols-outlined service-icon">code</span>
                <div class="card-content">
                    <h2>Web Development</h2>
                    <p>
                        Building responsive and dynamic websites using the latest
                        technologies like Vue.js and Django.
                    </p>
                </div>
                <div class="card-skills">
                    <span>HTML</span>
                    <span>CSS</span>
                    <span>JavaScript</span>
                    <span>Vue.js</span>
                    <span>Django</span>
                    <span>SQL</span>
                </div>

            </div>
            <!-- Service Card 2: IT Support-->
            <div class="service-card">
                <span class="material-symbols-outlined service-icon">support_agent</span>
                <div class="card-content">
                    <h2>IT Support</h2>
                    <p>
                        Offering reliable IT support services including troubleshooting,
                        maintenance, and network management.
                    </p>
                </div>
                <div class="card-skills">
                    <span>Network Setup</span>
                    <span>Troubleshooting</span>
                    <span>Maintenance</span>
                    <span>Security</span>
                </div>
            </div>
            <!-- Service Card 3: Database Management-->
            <div class="service-card">
                <span class="material-symbols-outlined service-icon">storage</span>
                <div class="card-content">
                    <h2>Database Management</h2>
                    <p>
                        Designing and maintaining efficient database systems to ensure
                        data integrity and performance.
                    </p>
                </div>
                <div class="card-skills">
                    <span>SQL</span>
                    <span>Data Modeling</span>
                    <span>Backup & Recovery</span>
                </div>
            </div>
        </div>
        <!-- CTA Button -->
        <div>
            <button>Let's Work Together</button>
        </div>
    </main>
</template>

<style scoped lang="scss">
main {
    padding: {
        top: 3rem;
        bottom: 4rem;
    }
}

.page-title {
    font: {
        size: 2.5rem;
        weight: 900;
    }

    letter-spacing: -0.033rem;
    line-height: 1.25;
    color: rgb(15, 23, 42);
}

.page-summary {
    font: {
        size: 1rem;
        weight: 400;
    }

    line-height: 1.5;
    color: rgb(71, 85, 105);
    padding: 2rem 1rem;
}

.services-container {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 1.5rem;
    padding: 1rem;

    @media (min-width: 768px) {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    @media (min-width: 1024px) {
        grid-template-columns: repeat(3, minmax(0, 1fr));
    }
}

.service-card {
    display: flex;
    flex: 1 1 0%;
    flex-direction: column;
    gap: 1rem;
    padding: 1.5rem;
    border: 1px solid rgb(226, 232, 240);
    border-radius: 0.75rem;
    box-shadow: 0 1px 2px rgb(0 0 0 / 0.05);
    background-color: rgb(255, 255, 255);
    transition: all 300ms ease-in-out;

    &:hover {
        box-shadow: 0 4px 6px rgb(0 0 0 / 0.1);
    }
}

.service-icon {
    font-size: 1.875rem;
    color: rgb(59, 130, 246);
}

.card-content {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;

    h2 {
        font: {
            size: 1.25rem;
            weight: 700;
        }

        color: rgb(15, 23, 42);
        line-height: 1.25;
    }

    p {
        font: {
            size: 1rem;
            weight: 400;
        }

        color: rgb(100, 116, 139);
        line-height: 1.5;
    }
}

.card-skills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    padding-top: 0.5rem;

    span {
        background-color: rgb(239, 246, 255);
        color: rgb(37, 99, 235);
        font: {
            size: 0.875rem;
            weight: 500;
        }
        padding: 0.25rem 0.75rem;
        border-radius: 0.375rem;
        line-height: 1;
    }
}
</style>
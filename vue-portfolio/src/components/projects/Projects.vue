<script setup>
import { ref, computed } from "vue";
import healthMgtSystem from "@/assets/images/health-mgt-system.png";
import wasteMgtSystem from "@/assets/images/waste-mgt-system.jpg";
import zeeliu from "@/assets/images/zeeliu.png";
import webScraping from "@/assets/images/web-scraping.jpg";
import dataWrangling from "@/assets/images/data-wrangling.jpg";

const selectedCategory = ref("All");

const projects = ref([
  {
    id: 1,
    title: "Health Management System",
    description:
      "This project demonstrates how AI can be integrated into modern web applications through an automated appointment booking system with SMS notifications. It incorporates key features such as AWS cloud storage for scalable data management and two-factor authentication to enhance security. This system was developed as my final year project at MKU University.",
    technologies: "JavaScript, PHP, MariaDB, AWS, OpenAI",
    image: healthMgtSystem,
    category: "Web Development",
  },
  {
    id: 2,
    title: "Waste Management System",
    description:
      "In this project, I served as the backend developer, implementing key admin features, authentication mechanisms, and database architecture and modeling. While the frontend was handled by another developer, I also contributed as a consultant to ensure seamless integration. This role highlighted my expertise in building secure, scalable backend systems for collaborative development environments.",
    technologies: "JavaScript, PHP, MariaDB",
    image: wasteMgtSystem,
    category: "Web Development",
  },
  {
    id: 3,
    title: "Zeeliu Designs",
    description:
      "This project involved developing a website based on a provided design specification. I was responsible for building the site and ensuring that the content and layout were properly aligned and visually consistent. The website was optimized to function seamlessly across both desktop and mobile views.",
    technologies: "HTML, CSS, BootStrap, JavaScript",
    image: zeeliu,
    category: "Web Development",
  },
  {
    id: 4,
    title: "Web Scraping using Python",
    description:
      "Developed a web scraping solution to automatically extract, clean, and organize data from targeted websites for efficient analysis and reporting.",
    technologies: "Python, Google Colab",
    image: webScraping,
    category: "Data Analysis",
  },
  {
    id: 5,
    title: "Netflix Data Wrangling",
    description:
      "Performed data wrangling on a Netflix dataset to clean, transform, and prepare the data for exploratory analysis and insights generation.",
    technologies: "Python, Kaggle",
    image: dataWrangling,
    category: "Data Analysis",
  },
]);

const filteredProjects = computed(() => {
  if (selectedCategory.value === "All") {
    return projects.value;
  }
  return projects.value.filter(
    (project) => project.category === selectedCategory.value
  );
});
</script>

<template>
    <main>
        <!-- PageHeading -->
        <div class="page-heading">
            <div>
                <p>Projects</p>
                <p>Below are a few projects I have worked on.</p>
            </div>
        </div>
        <!-- Chips -->
        <div class="button-group">
            <button 
                @click="selectedCategory = 'All'"
                :class="{ active: selectedCategory === 'All' }">
                <span>All</span>
            </button>
            <button 
                @click="selectedCategory = 'Web Development'"
                :class="{ active: selectedCategory === 'Web Development' }">
                <span>Web Development</span>
            </button>
            <button 
                @click="selectedCategory = 'Data Analysis'"
                :class="{ active: selectedCategory === 'Data Analysis' }">
                <span>Data Analysis</span>
            </button>
        </div>
        <!-- ImageGrid -->
        <div class="image-grid">
            <!-- Project Item -->
            <div class="project-item" v-for="project in filteredProjects" :key="project.id">
                <div>
                    <div :style="{ backgroundImage: `url(${project.image})` }"></div>
                </div>
                <div>
                    <p>{{ project.title }}</p>
                    <p>{{ project.description }}</p>
                    <p>{{ project.technologies }}</p>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
main {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    padding: 1rem 2rem;

    @media (min-width: 640px) {
        padding: 1.5rem 0;
    }

    @media (min-width: 768px) {
        padding: 2.5rem 0;
    }
}

.page-heading {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 0.75rem;

    div {
        display: flex;
        min-width: 18rem;
        flex-direction: column;
        gap: 0.5rem;

        p:first-child {
            font: {
                size: 2.25rem;
                weight: 900;
            }

            color: rgb(17, 24, 39);
        }

        p:last-child {
            font: {
                size: 1rem;
                weight: 400;
            }

            color: rgb(107, 114, 128);
        }
    }
}

.button-group {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    padding: 0.25rem;

    button {
        display: flex;
        flex-shrink: 0;
        height: 2rem;
        align-items: center;
        justify-content: center;
        column-gap: 0.5rem;
        border-radius: 9999px;
        background-color: rgb(19, 91, 236, 0.2);
        padding: 0 1rem;
        border: none;
        cursor: pointer;
        transition: all 0.3s ease;

        &:hover {
            background-color: rgb(19, 91, 236, 0.4);
        }

        &.active {
            background-color: rgb(19, 91, 236);
        }

        &.active span {
            color: white;
        }

        span {
            font: {
                size: 0.875rem;
                weight: 500;
            }

            color: rgb(19, 91, 236);
            line-height: 1.5;
            transition: color 0.3s ease;
        }
    }
}

.image-grid {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    gap: 1.5rem;

    @media (min-width: 640px) {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    @media (min-width: 768px) {
        grid-template-columns: repeat(3, minmax(0, 1fr));
    }
}

.project-item {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    border-radius: 0.5rem;
    background-color: rgb(255, 255, 255);
    padding: 1rem;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;

    &:hover {
        box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        transform: translateY(-4px);
    }

    div:first-child {
        width: 100%;
        overflow: hidden;
        border-radius: 0.375rem;

        div {
            width: 100%;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            aspect-ratio: 16 / 9;
            transition: transform 0.3s ease;

            &:hover {
                transform: scale(1.05);
            }
        }
    }

    div:last-child {
        p:first-child {
            font: {
                size: 1rem;
                weight: 500;
            }

            color: rgb(17, 24, 39);
        }

        p:nth-child(2) {
            font: {
                size: 0.875rem;
                weight: 400;
            }

            color: rgb(107, 114, 128);
            line-height: 1.5;
            margin-top: 0.25rem;
        }

        p:last-child {
            font: {
                size: 0.75rem;
                weight: 400;
            }

            margin-top: 0.5rem;
            color: rgb(96, 165, 250);
        }
    }
}
</style>
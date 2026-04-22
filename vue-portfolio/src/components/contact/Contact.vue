<template>
    <main>
        <!-- Page Header -->
        <div class="page-header">
            <div>
                <p>Get in Touch</p>
                <p>Have a project in mind, a question, or just want to say hello? I'd love to hear from you.</p>
            </div>
        </div>
        <div class="contact-content">
            <!-- Contact Form -->
            <div class="contact-form">
                <h2>Send a Direct Message</h2>
                <form>
                    <div>
                        <label for="name">
                            <p>Name</p>
                            <input id="name" placeholder="Enter your name" />
                        </label>
                        <label for="name">
                            <p>Email</p>
                            <input id="email" placeholder="Enter your email address" />
                        </label>
                    </div>
                    <label for="subject">
                        <p>Subject</p>
                        <input id="subject" placeholder="What is this about?" />
                    </label>
                    <label for="message">
                        <p>Your Message</p>
                        <textarea id="message" placeholder="Enter your message here..."></textarea>
                    </label>
                    <button type="submit">Send Message</button>
                </form>
            </div>
            <!-- Contact Information -->
            <div>
                <h2>Other Ways to Reach Me</h2>
                <div>
                    <h3>On Social Media</h3>
                    <div>
                        <a href="#">LinkedIn Icon here...</a>
                        <a href="#">Github Icon here...</a>
                        <a href="#">Twitter Icon here...</a>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
main {
    display: flex;
    padding: 3rem 0;
    flex-direction: column;

    @media (min-width: 1024px) {
        padding: 5rem 0;
    }
}

.page-header {
    display: flex;
    flex-wrap: wrap;
    padding: 1rem;

    div {
        display: flex;
        flex-direction: column;
        max-width: 32rem;
        gap: 0.75rem;

        p:first-child {
            color: rgb(17, 24, 39);
            font-size: 2.25rem;
            font-weight: 900;
            line-height: 1.25;
            letter-spacing: -0.033em;

            @media (min-width: 640px) {
                font-size: 3rem;
                line-height: 1;
            }
        }

        p:last-child {
            font-size: 1rem;
            font-weight: 400;
            color: rgb(107, 114, 128);
            line-height: 1.5;
        }
    }
}

.contact-content {
    margin-top: 2rem;
    display: grid;
    gap: 3rem;
    grid-template-columns: repeat(1, minmax(0, 1fr));

    @media (min-width: 1024px) {
        grid-template-columns: repeat(5, minmax(0, 1fr));
        gap: 6rem;
    }
}

.contact-form {
    grid-column: span 3 / span 3;

    h2 {
        padding: 1.25rem 1rem 0.75rem 1rem;
    }
}

form {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding: 1rem;

    div {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;

        @media (min-width: 640px) {
            flex-direction: row;
            gap: 1rem;
        }
    }
}

label {
    display: flex;
    flex-direction: column;
    flex: 1;

    p {
        font-size: 1rem;
        font-weight: 500;
        color: rgb(31, 41, 55);
        line-height: 1.5;
        padding-bottom: 0.5rem;
    }

    input,
    textarea {
        display: flex;
        width: 100%;
        min-width: 0;
        flex: 1;
        resize: none;
        overflow: hidden;
        border-radius: 0.5rem; // rounded-lg
        color: #1f2937; // text-gray-800
        background-color: #f9fafb; // bg-background-light (adjust if custom)
        border: 1px solid #d1d5db; // border-gray-300
        height: 3.5rem; // h-14
        padding: 15px; // p-[15px]
        font-size: 1rem; // text-base
        font-weight: 400; // font-normal
        line-height: 1.5; // leading-normal
        font-family: inherit; // Use page's font family
        transition: all 0.2s ease-in-out;

        &::placeholder {
            color: #9ca3af; // placeholder:text-gray-400
            font-family: inherit; // Use page's font family
        }

        &:focus {
            outline: none;
            box-shadow: 0 0 0 2px rgba(59, 130, 246, 0.5); // focus:ring-primary/50 (approx)
        }
    }
}

button {
    display: flex;
    align-items: center;
    justify-content: center;
    min-width: 84px;
    width: 100%;
    overflow: hidden;
    border-radius: 0.5rem; // rounded-lg
    height: 3rem;
    padding: 0 1.5rem;
    background-color: #135bec; // bg-primary
    color: #ffffff; // text-white
    font-size: 1rem; // text-base
    font-weight: 700; // font-bold
    line-height: 1.5; // leading-normal
    letter-spacing: 0.015rem;
    border: none;

    &:hover {
        background-color: rgba(59, 130, 246, 0.9); // hover:bg-primary/90
    }

    @media (min-width: 640px) {
        min-width: auto;
    }

    span {
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
}
</style>
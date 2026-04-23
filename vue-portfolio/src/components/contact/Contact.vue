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
            <div class="contact-info">
                <h2>Other Ways to Reach Me</h2>
                <div class="contact-details">
                    <h3>On Social Media</h3>
                    <div>
                        <a href="https://www.linkedin.com/in/ndwigadave/"><svg aria-hidden="true" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                                <path clip-rule="evenodd"
                                    d="M16.338 16.338H13.67V12.16c0-.995-.017-2.277-1.387-2.277-1.388 0-1.601 1.086-1.601 2.206v4.248H8.014V8.59h2.559v1.174h.037c.356-.675 1.227-1.387 2.526-1.387 2.703 0 3.203 1.778 3.203 4.092v4.711zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 114.128 0c0 1.14-.931 2.065-2.065 2.065zm1.336 8.905H4.002V8.59h2.671v7.748zM17.638 2H6.362A4.362 4.362 0 002 6.362v11.276A4.362 4.362 0 006.362 22h11.276A4.362 4.362 0 0022 17.638V6.362A4.362 4.362 0 0017.638 2z"
                                    fill-rule="evenodd"></path>
                            </svg></a>
                        <a href="https://github.com/Dave-Njeru"> <svg aria-hidden="true" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                                <path clip-rule="evenodd"
                                    d="M12 2C6.477 2 2 6.477 2 12c0 4.286 2.89 7.92 6.837 9.163.498.09.68-.216.68-.48 0-.236-.008-.864-.013-1.695-2.804.604-3.396-1.35-3.396-1.35-.452-1.15-1.104-1.455-1.104-1.455-.903-.618.068-.605.068-.605 1.0.07 1.527 1.025 1.527 1.025.888 1.523 2.327 1.083 2.895.828.09-.643.348-1.083.633-1.33-2.21-.25-4.533-1.102-4.533-4.924 0-1.087.39-1.978 1.028-2.675-.104-.253-.446-1.267.098-2.638 0 0 .837-.268 2.742 1.022A9.63 9.63 0 0112 6.82c.85.004 1.705.114 2.504.336 1.905-1.29 2.74-1.022 2.74-1.022.546 1.37.202 2.385.1 2.638.64.697 1.026 1.588 1.026 2.675 0 3.833-2.327 4.67-4.542 4.914.357.308.678.918.678 1.85 0 1.335-.012 2.415-.012 2.742 0 .267.18.577.688.48A10.007 10.007 0 0022 12c0-5.523-4.477-10-10-10z"
                                    fill-rule="evenodd"></path>
                            </svg></a>
                        <a href="https://x.com/DaveNdwiga"> <svg aria-hidden="true" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                                <path
                                    d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z">
                                </path>
                            </svg></a>
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

.contact-info {
    grid-column: span 2 / span 2;

    h2 {
        color: #111827; // text-gray-900
        font-size: 22px; // text-[22px]
        font-weight: 700; // font-bold
        line-height: 1.25; // leading-tight
        letter-spacing: -0.015em; // tracking-[-0.015em]
    }
}

.contact-details {
    padding-top: 1rem;

    h3 {
        font-size: 1.125rem;
        line-height: 1.75rem;
        font-weight: 700;
        color: rgb(17, 24, 39);
    }

    div {
        display: flex;
        gap: 1rem;
        align-items: center;

        a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 2.5rem;
            height: 2.5rem;
            border-radius: 9999px; // rounded-full
            background-color: #e5e7eb; // bg-gray-200
            color: #4b5563; // text-gray-600
            transition: all 0.3s;

            svg {
                display: block;
                width: 1.5rem;
                height: 1.5rem;
            }

            &:hover {
                background-color: #135bec; // hover:bg-primary
                color: #ffffff; // hover:text-white
            }
        }
    }
}
</style>
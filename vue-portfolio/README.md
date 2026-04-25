# vue-portfolio

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Recommended Browser Setup

- Chromium-based browsers (Chrome, Edge, Brave, etc.):
  - [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
  - [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)
- Firefox:
  - [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
  - [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

## Deployment

This project is configured for deployment on [Vercel](https://vercel.com/). The `vercel.json` file contains the deployment configuration.

### Vercel Configuration (`vercel.json`)

The `vercel.json` file defines how the application should be deployed on Vercel:

```json
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}
```

**Explanation:**

- **Rewrites**: This configuration tells Vercel to rewrite all incoming requests (`/(.*)`) to `/index.html`. This is essential for Single Page Applications (SPAs) built with Vue.js, as it ensures that client-side routing works correctly.
- When a user navigates to any route (e.g., `/about`, `/projects`), Vercel serves the `index.html` file, allowing Vue Router to handle the routing on the client side.
- Without this configuration, direct navigation to routes other than the root would result in 404 errors, as the server wouldn't find corresponding files.

**Why this is needed:**

- Vue.js applications use client-side routing, meaning all routes are handled by JavaScript in the browser.
- Server-side routing expects physical files for each route, which doesn't exist in SPAs.
- The rewrite rule ensures that all routes are served by the main `index.html` file, enabling proper SPA functionality.

To deploy:

1. Push your code to a Git repository (GitHub, GitLab, etc.)
2. Connect your repository to Vercel
3. Vercel will automatically detect the `vercel.json` file and apply the configuration
4. Your Vue portfolio will be live with proper routing!

## Code Formatting

This project uses [Prettier](https://prettier.io/) for consistent code formatting. The configuration is defined in `.prettierrc.json`.

### Prettier Configuration (`.prettierrc.json`)

The `.prettierrc.json` file contains the following configuration:

```json
{
  "quoteProps": "preserve"
}
```

**Explanation:**

- **quoteProps**: Set to `"preserve"`, this option tells Prettier to keep the original quote style for object properties instead of enforcing a consistent style.
- This means if you write `{"name": "John"}` or `{name: "John"}`, Prettier will leave the quotes as they are rather than converting them to a uniform style.
- This setting provides flexibility in coding style while still maintaining other formatting consistency.

**Usage:**

- Prettier will automatically format your code when you save files (if configured in your IDE)
- You can also run Prettier manually: `npx prettier --write .`
- To check formatting without making changes: `npx prettier --check .`

This configuration helps maintain code readability while respecting individual preferences for property quoting in JavaScript/TypeScript objects.

# The Fundamentals

An interactive course that teaches how software works — from databases to shipping a product. No prerequisites. No fluff.

**[the-fundamentals-eight.vercel.app](https://the-fundamentals-eight.vercel.app)**

## Why this exists

Most "learn to code" resources teach you *how* to type syntax. They skip the harder question: how does all of this actually work together?

The Fundamentals walks through a real production codebase ([Paperclip](https://github.com/paperclipai/paperclip)) and uses it as the connective thread across 12 courses. By the end, you understand the full stack — not because you memorized APIs, but because you traced one task from a button click through HTTP, middleware, services, a database, and back.

## The courses

01. **How Databases Work** — Tables, keys, relationships, queries, and schema.
02. **The Codebase** — How a real 2,000-file production app is organized.
03. **APIs & HTTP** — Requests, responses, methods, status codes, JSON, REST.
04. **Build a Mini App** — Three files. One working app. Database, server, UI.
05. **How Deployment Works** — localhost to live URL. DNS, CDN, environments.
06. **How Git Works** — Commits, branches, merging, pull requests.
07. **How Auth Works** — Passwords, hashing, sessions, JWTs, OAuth, API keys.
08. **How TypeScript Works** — Types, interfaces, generics, and why they matter.
09. **How React Works** — Components, state, props, effects, the render cycle.
10. **How Testing Works** — Unit, integration, E2E, mocking, TDD.
11. **How AI Agents Work** — LLMs, prompts, tool use, the agent loop, costs.
12. **How to Ship a Product** — MVP, stack decisions, launch, users, monitoring.

## Run it

```
npx serve .
```

## Deploy it

```
vercel --prod
```

## Add a course

Every course is a single HTML file in `lessons/`. The shared infrastructure handles the sidebar, theme, search, copy buttons, and progress tracking — you just write the content.

To add Course 13:

1. Create `lessons/your-course.html` following the structure of any existing course.
2. Use CSS variables from `css/shared.css` for all colors — never hardcode hex.
3. Include the sidebar HTML with all courses listed (copy from an existing file).
4. Add your course to the sidebar in every other lesson file and `index.html`.
5. Add your course to the `courseIndex` array in `js/shared.js`.
6. Add a card to the course grid in `index.html`.
7. Update the "Next Course" banner in the preceding course to link to yours.

## License

MIT

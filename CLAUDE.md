# The Fundamentals

12 interactive courses teaching how software works. Static site deployed to Vercel.

## Decisions

- **No framework.** Static HTML, CSS, vanilla JS. No build step. This is intentional — the app teaches fundamentals, so the app itself should be fundamental. Don't add React, Next.js, or a bundler.
- **One file per course.** Each course is a single self-contained HTML file. The tradeoff (large files, repeated sidebar HTML) is worth the simplicity.
- **Paperclip is the connective thread.** Every course references the Paperclip codebase (~/paperclip) as its running example. Databases use Paperclip tables. The codebase tutorial walks Paperclip's actual file structure. Don't introduce unrelated example apps.
- **CSS variables for all colors.** Light/dark theming works because every color is a variable. If you hardcode a hex value, the theme breaks. No exceptions.

## Constraints

- Sidebar HTML is duplicated in every file. When adding a course, you must update the sidebar in all 12 existing files + index.html.
- The `courseIndex` array in `js/shared.js` powers Cmd+K search. It must match the actual courses.
- Some files use `.nav` for the top bar, others use `.top-nav`. Either is fine — just match whichever the file already uses.
- Code blocks need class `code-block` to get auto-injected copy buttons. Don't add copy buttons manually.
- The top nav is `position: fixed` and needs `left: 280px` at desktop widths to clear the sidebar.

## Deploy

```
vercel --prod
```

Production: https://the-fundamentals-eight.vercel.app
Vercel project: jared-2093s-projects/the-fundamentals

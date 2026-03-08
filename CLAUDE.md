# CLAUDE.md

## Project

ifupdown.com is the landing page for ifupdown.com. It is a single self-contained `index.html` file with no external dependencies — all CSS, SVG, and JS are inlined.

## Architecture

- **Single file**: Everything lives in `index.html`. No build tools, no bundler, no external CSS/JS/images. The file must remain fully self-contained so it can be deployed by copying a single file.
- **Inline SVG logo**: Geometric up/down triangles with horizontal offset.
- **Canvas particle effect**: Vanilla JS particle animation around the logo area (no libraries).
- **Dark mode**: Via `prefers-color-scheme` media query with CSS custom properties.
- **Dynamic copyright year**: Inline `<script>` sets the year in the footer.

## Commits

- Use **conventional commits** (e.g., `feat:`, `fix:`, `style:`, `refactor:`, `chore:`, `docs:`).
- Keep commit messages concise — one line summary, optional body for context.

## Branching

- `main` is the production branch.
- For novel changes or new features, create a feature branch and open a pull request.
- Trivial fixes (typos, small style tweaks) can go directly to `main`.

## Constraints

- **No external dependencies**: No CDN links, no external fonts, no analytics, no tracking. Everything must be inlined.
- **Responsive**: Must work on mobile without a separate stylesheet or breakpoint file.
- **Accessible**: Respect `prefers-reduced-motion` and `prefers-color-scheme`. Use semantic HTML.
- **History comments**: Preserve the date history comment block in `<head>` and add a new entry for significant updates.

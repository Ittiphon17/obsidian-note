<!-- BEGIN:nextjs-agent-rules -->
# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->

# Agent Guidelines & Project Rules

This document outlines instructions, patterns, and constraints that AI coding agents must follow when modifying or extending this codebase.

---

## 1. Core Tech Stack Constraints

### Next.js 16+ & React 19
- **App Router:** All pages must reside within `src/app/`.
- **Client Components:** Use `"use client"` strictly at the top of files that utilize React hooks (`useState`, `useEffect`) or animation libraries (`framer-motion`). Keep Server Components as the default.
- **Rendering & Data Fetching:** Do not use legacy methods like `getServerSideProps` or `getStaticProps`.

### Tailwind CSS v4
- **PostCSS integration:** Tailwind CSS v4 is configured using `@tailwindcss/postcss` and raw CSS imports.
- **Styling Standards:** Avoid hardcoding static color codes or arbitrary utility overrides if a theme-based token is available. Maintain consistency with the existing dark aesthetic (e.g., `#0a0a0a` background, soft borders, and blurred glow circles).

---

## 2. UI & Aesthetic Requirements

- **Theme Integrity:** Keep the UI strictly dark-themed. Background colors must remain consistent with `#0a0a0a` or `#0d0d0d`.
- **Bento Grid Design:** When adding layout elements, align them with the Apple-style/Bento-style card pattern using the `<BentoCard>` component.
- **Animations:**
  - Use `framer-motion` for transitions.
  - Keep animations subtle, quick, and non-blocking (e.g., duration ≤ 0.5s).
  - Use staggered animations (`delay: index * 0.15`) for list displays (e.g., experiences, projects) to enhance perceived performance.
- **Images:** Always use the Next.js `<Image>` component from `next/image`.
  - Always verify image paths and file extensions in `public/assets/` before implementing.
  - Apply `priority` prop to above-the-fold images to optimize LCP.

---

## 3. Code Quality & Standards

- **TypeScript:** Type safety is mandatory. Do not use `any`. Define proper interfaces for component props.
- **Icons:** Use `lucide-react` for UI icons. Always specify width and height classes (e.g. `className="w-4 h-4"`).
- **Separation of Concerns:** Avoid hardcoding massive arrays of data (e.g., projects, experiences) directly inside UI components. Move data structures to separate modules or config files when scaling.
- **Clean Dev Workflow:** Always test changes by building the application (`npm run build`) or running the linter (`npm run lint`) to ensure type-safety and rule compliance.

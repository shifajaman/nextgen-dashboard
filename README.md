# Next-Gen Learning Platform Dashboard

A premium, modern bento-grid dashboard built with Next.js, Tailwind CSS, and Supabase.

## Architectural Choices
- **Server/Client Component Split:** Data fetching is handled entirely on the server level inside `page.tsx` using Next.js Server Components. This keeps our Supabase connection secure, reduces client-side JavaScript, and leverages server-side rendering for optimal performance.
- **Decoupled UI Components:** Visual presentation layers (`BentoGrid.tsx`, `CourseCard.tsx`) are completely decoupled from data-fetching logic, establishing a clean, logical, and maintainable component tree.
- **Fluid Responsiveness:** Utilizes Tailwind CSS native breakpoints to dynamically transition from a multi-column desktop layout to a single-column stacked layout on mobile screens (< 768px).

## Environment Setup
Copy the `.env.example` file to `.env` and populate your credentials:
- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

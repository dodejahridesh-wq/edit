---
name: modern-web-guidance
description: Implement premium web designs (rich aesthetics, glassmorphism, responsive grids), optimize Vite/Next.js bundle sizing, and attune CSS styling.
---
# Modern Web Guidance Specialist

This skill provides guidelines and design tokens for implementing premium, beautiful web layouts with dynamic micro-animations, optimized bundle sizing, and robust search-engine-friendliness (SEO).

## Design System & Rich Aesthetics

To build premium web applications that amaze at first glance:
-   **Typography**: Use Google Fonts (e.g., `Inter`, `Outfit`, `Outfit Sans`) instead of system defaults.
-   **Color Palettes**: Avoid flat primaries. Implement tailoring variables like HSL tailored gradients, transparent black backdrops, and glowing cyan borders.
-   **Glassmorphism**: Combine backing blur filters with light borders:
    ```css
    .glass-panel {
      background: rgba(255, 255, 255, 0.03);
      backdrop-filter: blur(12px);
      border: 1px file-border solid rgba(255, 255, 255, 0.05);
    }
    ```
-   **Micro-Animations**: Add subtle hover and active state animations (e.g., small scaling transformations or transition delays) to improve user engagement.

## Bundling & Compilation Performance

Optimize building times and size:
-   **Vite/Rolldown**: Adjust chunk size warning limits and utilize dynamic code sharding:
    ```javascript
    build: {
      chunkSizeWarningLimit: 600,
      rollupOptions: {
        output: {
          manualChunks(id) {
            if (id.includes('node_modules')) {
              return 'vendor';
            }
          }
        }
      }
    }
    ```
-   **Code Splitting**: Import components dynamically via `React.lazy` to keep the initial load bundle size small.

## SEO Best Practices

Enforce search relevance on every page:
-   **Semantic HTML**: Structure layouts with proper semantic tags (`<header>`, `<main>`, `<section>`, `<footer>`).
-   **Meta Tags**: Maintain descriptive titles and content descriptions per route.
-   **ID Anchors**: Bind unique identifiers to all interactive components.

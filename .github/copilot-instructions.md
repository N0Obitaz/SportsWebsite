# Copilot Instructions for SportsWebsite

This project is a static sports association website built with a single HTML file (`index.html`). It uses Tailwind CSS for styling and leverages external JS libraries for UI effects and icons.

## Project Architecture
- **Single-page static site**: All content and UI logic reside in `index.html`.
- **No build system or backend**: There are no scripts, package managers, or server-side code. All dependencies are loaded via CDN.
- **External dependencies**:
  - [Tailwind CSS](https://cdn.tailwindcss.com) for utility-first styling
  - [AOS (Animate On Scroll)](https://unpkg.com/aos@2.3.1/dist/aos.js) for scroll animations
  - [Feather Icons](https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js) for SVG icons

## Key UI Patterns
- **Navigation bar**: Responsive, with mobile menu icon (no JS logic for menu toggling yet)
- **Hero section**: Uses gradient backgrounds and large typography
- **Featured sports/events/testimonials**: Card-based layout with Tailwind classes and AOS animation attributes
- **Footer**: Multi-column layout with social icons (Feather)
- **Custom CSS**: Minimal, for gradients and hover scaling

## Developer Workflow
- **Edit `index.html` directly** for all changes
- **Preview locally** by opening `index.html` in a browser
- **No build/test commands**; changes are visible immediately
- **Add new sections** by following the card/grid patterns and using Tailwind utility classes
- **Use CDN links** for any new JS/CSS libraries

## Project Conventions
- **Class naming**: Use Tailwind utility classes for layout, color, and spacing
- **Animations**: Add `data-aos` attributes for scroll-based animations
- **Icons**: Use `<i data-feather="icon-name">` and call `feather.replace()` in a script block
- **Responsiveness**: Use Tailwind's responsive prefixes (`sm:`, `md:`, `lg:`) for layouts
- **No custom JS logic** except for initializing AOS and Feather Icons

## Example: Adding a New Sport Card
```html
<div class="bg-white rounded-lg shadow-md overflow-hidden hover-scale" data-aos="fade-up" data-aos-delay="400">
  <img src="..." alt="Sport Name" class="w-full h-48 object-cover">
  <div class="p-6">
    <div class="flex items-center">
      <div class="flex-shrink-0 bg-blue-500 rounded-md p-2">
        <i data-feather="icon-name" class="text-white h-6 w-6"></i>
      </div>
      <div class="ml-4">
        <h3 class="text-lg font-medium text-gray-900">Sport Name</h3>
      </div>
    </div>
    <p class="mt-4 text-gray-600">Description here.</p>
  </div>
</div>
```

## Key File
- `index.html`: All code and content

---
For major changes, maintain the single-file structure and use CDN links for any new dependencies. If you add new files, update this document to reflect the new architecture.

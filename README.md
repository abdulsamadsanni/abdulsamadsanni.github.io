# abdulsamadsanni.github.io

My portfolio, built as an interactive late-night study desk.

**Live site:** [abdulsamadsanni.github.io](https://abdulsamadsanni.github.io)

## The concept

Instead of a template, the site is a single hand-drawn SVG scene: a desk at night facing a city window. Every object on the desk is real navigation. The book stack opens Projects, the leaning books open About Me and Interests, the spiral notebook opens Notes, the envelope opens Contact, and the portfolio case on the floor opens a gallery of my illustration work. Clicking any of them zooms the camera into the monitor, where the section opens as an on-screen window. The clock on the monitor shows your actual local time.

## How it is built

No frameworks, no build step, no dependencies. One HTML file containing:

- **A layered SVG illustration** drawn by hand in code: three parallax layers (wall, floor, desk) that shift subtly with the mouse.
- **CSS-driven interaction.** Each clickable item uses a two-group pattern: an outer group holds the SVG positioning transform, an inner group receives the CSS hover transform. Keeping them separate prevents the CSS transform from overwriting the item's placement (a common SVG pitfall).
- **A zoom-to-monitor transition.** Opening a section scales the whole scene toward the monitor's coordinates via a single CSS transform, then reveals the content as a dialog styled as an application window.
- **Vanilla JavaScript** for the live clock, open/close logic, keyboard handling, and parallax. Roughly 80 lines.

## Accessibility

- Every interactive object has `role="button"`, a descriptive `aria-label`, and full keyboard support (Tab, Enter, Space, Escape).
- A plain button navigation sits below the scene as the primary path on small screens.
- `prefers-reduced-motion` is respected: parallax, zoom, steam, and twinkle animations all switch off.

## Running locally

Clone and open `index.html` in a browser. That is the entire setup.

## About me

Fourth-year Computer Science student at Carleton University focused on applied machine learning and computer vision, with a background in graphic design. Seeking a Fall 2026 co-op.

- [GitHub](https://github.com/abdulsamadsanni)
- Contact details are in the envelope on the desk.

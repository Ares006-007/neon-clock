<img width="831" height="581" alt="image" src="https://github.com/user-attachments/assets/99772339-a6b3-4fe9-a570-4ac2809ebd36" />


# Neon 3D Digital Clock

A responsive neon-style 3D digital clock built with **HTML**, CSS, and vanilla JavaScript. The clock uses a custom seven‑segment display, 3D transforms, and neon lighting effects to create a futuristic look.

> **Live demo:** https://ares006-007.github.io/neon-clock/

## Features

- Real‑time digital clock (hours, minutes, seconds) that updates every second using the `Date` API
- Custom seven‑segment digits built from dynamic DOM elements (`<figure>` and `<span>`). Each segment is controlled via `data-digit` attributes and CSS.
- 3D camera rotation and subtle panning using `camera-rotate` and `camera-pan` keyframe animations.
- Neon glow, soft shadows, and blurred reflections for a realistic glowing effect.
- Hue rotation through the HSL color wheel for smooth color transitions.
- Safari/iOS-specific handling to avoid transition issues on WebKit browsers.

## Demo

You can see the clock running live here:

- Live demo: https://ares006-007.github.io/neon-clock/

Open it in any modern browser for the full 3D and animation effects.

## Project Structure

- `index.html` – Base markup with the wrapper and `<main>` element where the clock digits and colons are injected.
- `style.css` – All styling for layout, 3D perspective, seven‑segment shapes, neon glow, shadows, reflections, and animations.
- `script.js` – JavaScript that creates digit groups, colon separators, manages shadows, and updates the time via `requestAnimationFrame`.

## How It Works

### Digit Generation

- A `bars` configuration defines the seven segments (`end`, `side`, `middle`) with modifiers like `top`, `bottom`, `left`, `right`.
- For each digit, the script creates a `<figure>` with multiple `<span>` segments and sets a `data-digit` attribute.
- CSS uses selectors like `.digit[data-digit="0"]` and a CSS variable `--act` to toggle which segments are visible for each number.

### Time Logic

- On init, the script reads the current hours, minutes, and seconds, and creates three digit groups separated by colon groups.
- An `update` function runs in a `requestAnimationFrame` loop, checking for changes in seconds.
- When seconds change, all three groups (main digits and their shadows) are updated to reflect the new time.

### Visual Effects and Animations

- The `body` and `.wrapper` elements use `perspective` and `transform-style: preserve-3d` to enable 3D transforms.
- `camera-rotate` animates the scene with a slow Y‑axis rotation, while `camera-pan` adds gentle positional movement.
- Shadows and reflections are created with duplicate digit groups (`shadow1`, `shadow2`), blur filters, and gradient masks.
- `hue-rotate` keyframes evolve the `color` property through 0–360 degrees for continuous color cycling.
- A user‑agent check adds a `.safari` class to simplify transitions and improve performance on Safari.

## Getting Started

1. Clone or download this repository.
2. Make sure the following files are in the same directory:
   - `index.html`
   - `style.css`
   - `script.js`
3. Open `index.html` directly in your browser, or run a simple static server (e.g., VS Code Live Server) and navigate to the served URL.

## Browser Support

This project targets modern browsers that support:

- CSS 3D transforms and `transform-style: preserve-3d`.
- CSS `filter`, `clip-path`, and keyframe animations.
- Modern JavaScript features like `requestAnimationFrame`, `classList`, and `String.prototype.padStart`.

Safari and iOS devices are supported with specific CSS/JS adjustments via the `.safari` body class.

## Customization

You can customize the clock by:

- Changing sizes (root `font-size`, digit heights, gaps) to scale the layout.
- Editing the `hue-rotate` keyframes or the base HSL variables (`--s`, `--l`) to alter color intensity and saturation.
- Adjusting animation durations for `camera-rotate` and `camera-pan` to make the motion faster or slower.
- Modifying the `bars` configuration or CSS segment shapes to explore alternative digit styles.


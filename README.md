# Neon Clock

> A stunning 3D neon digital clock with real-time updates, dynamic shadows, and immersive camera animations powered by vanilla JavaScript.

## Features

- **7-Segment Display** – Classic digital clock segments rendered with precise clip-path styling
- **Real-Time Updates** – Live HH:MM:SS display that updates every second using `requestAnimationFrame`
- **3D Perspective** – Immersive depth with `transform-style: preserve-3d` and perspective transforms
- **Dual Shadow Layers** – Realistic shadow effects with blur and gradient masking for cinematic depth
- **Smooth Animations** – Two continuous camera animations: a 40s rotating pan and a 30s dynamic translation
- **Neon Glow Effects** – Multi-layered drop-shadow filters creating authentic neon luminescence
- **Responsive Scaling** – Fully responsive viewport-based sizing with fluid typography
- **Safari Optimization** – Special handling for Safari browsers to ensure cross-platform performance
- **Smooth Transitions** – Cubic-bezier easing on segment transitions for polished feel
- **Dark Gradient Background** – Modern minimal aesthetic with subtle linear gradient

## Tech Stack

- **HTML5** – Semantic markup with dynamic DOM generation
- **CSS3** – Advanced features including 3D transforms, clip-paths, animations, and blend modes
- **Vanilla JavaScript** – Pure ES6+ with no dependencies; object-oriented architecture
- **Web APIs** – `requestAnimationFrame` for smooth 60fps updates, DOM manipulation
- **Google Fonts** – Nunito Sans for clean, modern typography

## Live Demo

[Live Demo](https://ares006-007.github.io/neon-clock/)

## Project Structure

```
neon-clock/
├── index.html          # Entry point with base styles and font imports
├── script.js           # Dynamic clock generation and real-time update logic
├── style.css           # 3D animations, neon effects, and responsive styling
└── README.md           # Project documentation
```

**File Descriptions:**

- **index.html** – Minimal HTML structure with Nunito Sans font import and base reset styles. Houses a simple `<main>` element where the clock is dynamically generated.

- **script.js** – Orchestrates the entire clock display. Creates 7-segment digit renderers with dual shadow layers, manages real-time updates via `requestAnimationFrame`, and includes Safari detection for compatibility.

- **style.css** – The visual heart of the project. Contains 3D transforms, animated camera panning, neon glow filters, shadow masking, and all responsive typography scaling.

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No external dependencies required

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Ares006-007/neon-clock.git
   cd neon-clock
   ```

2. **Open in your browser:**
   ```bash
   # Option 1: Direct file open
   open index.html
   
   # Option 2: Use a local server (recommended)
   python -m http.server 8000
   # Then navigate to http://localhost:8000
   ```

3. **Enjoy the show!** The clock will immediately begin displaying the current time with full 3D animations.

## Screenshots

![Neon Clock Preview](./screenshot.png)

## Contributing

I built this as a portfolio piece to showcase CSS mastery and 3D web design, but I'm open to creative enhancements. If you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

Potential areas for enhancement: color themes, time format options, additional animation modes, or mobile gestures.

## License

MIT License – Feel free to use this project for personal and commercial purposes. See [LICENSE](LICENSE) for details.

---

**Made by Ares** – A web developer obsessed with smooth animations and neon aesthetics.
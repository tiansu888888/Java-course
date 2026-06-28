# 🎨 Design System & Styling Architecture: Nanobanana V2

This document details the visual tokens, layout structures, and behavioral animations that compose the **Nanobanana V2: Macaron Glassmorphism Design System** used throughout the Java & Computer Systems Study Hub.

---

## 🎨 Color Palette & Variables

We discarded generic corporate blue and grey palettes in favor of a dreamy, high-end macaron pastel theme. Custom HSL-tailored CSS variables are exposed in the root selector:

```css
:root {
  /* Pastel Bases */
  --pastel-pink: #FFD1DC;
  --pastel-mint: #B0EACD;
  --pastel-blue: #AEC6CF;
  --pastel-lavender: #C3B1E1;
  --pastel-yellow: #FDFD96;
  
  /* Ink Typography (Strict Contrast) */
  --ink: #111111;       /* Deep Charcoal for high-contrast visibility */
  --ink-muted: #333333; /* Dark Grey for secondary text */
}
```

---

## 🫧 Glassmorphism Framework

All containers (cards, quiz questions, scenarios, coding blocks, matching grids) leverage a modern translucent frosted glass architecture:

```css
.card, .accordion, .quiz-card, .scenario-card {
  background: rgba(255, 255, 255, 0.45);
  border: 1px solid rgba(255, 255, 255, 0.6);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.07);
  border-radius: 32px;
  backdrop-filter: blur(40px);
  -webkit-backdrop-filter: blur(40px);
}
```
- **High Translucency:** The white background is set at `0.45` opacity to let the animated base gradient shine through softly.
- **Glass Border:** The border uses a higher opacity white (`0.6`) to define the container's structural boundaries cleanly.
- **Extreme Blur:** A `40px` backdrop filter ensures that background elements behind the card are completely out-of-focus, preventing text legibility issues.

---

## 🎭 Kinetic Layouts & Motion

### 1. Animated Base Gradient
The body background continuously transitions between the pastel color tokens using a slow keyframe loop:
```css
body {
  background: linear-gradient(135deg, var(--pastel-pink), var(--pastel-lavender), var(--pastel-blue), var(--pastel-mint));
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
}
@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
```

### 2. Floating Auras
Two massive, blurred radial gradients drift slowly in opposite directions in the viewport layer behind cards:
- `body::before` (Yellow aura, upper left, moving scale `1` to `1.2`).
- `body::after` (Pink aura, bottom right, moving scale `1.2` to `1` in reverse).

### 3. Transition Easings
Hover interactions on buttons, links, and option selections use an elegant, custom cubic-bezier spring curve:
```css
--spring: cubic-bezier(0.16, 1, 0.3, 1);
transition: all 0.4s var(--spring);
```

---

## ✏️ Typography Pairings

- **Headers:** `Orbitron` (sans-serif) — A futuristic, geometric typeface that provides high visual weight. Rendered in deep black ink.
- **Body & Controls:** `Rajdhani` (sans-serif) — A condensed, semi-square font that is extremely legible on bright pastel backgrounds.
- **Code:** `JetBrains Mono` (monospace) — Ideal for code blocks and blank completion inputs.

---

## 🌐 CSS Class-Driven Translation

To prevent bloating code templates, we implement a lightweight CSS-driven language state toggle. Elements with language designations are displayed or hidden based on a single body class:

```css
/* Default state (English) */
.lang-cn { display: none !important; }

/* Chinese state active */
body.cn-active .lang-en { display: none !important; }
body.cn-active .lang-cn { display: block !important; }
```
Using this architecture, the template elements (e.g. `<button>`, `<label>`) remain shared, while only the child language spans swap state, leading to a highly responsive and bug-free localization experience.

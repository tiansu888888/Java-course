# 🌐 Java Programming & Computer Systems Interactive Study Hub

> A premium, interactive, and bilingual (English/Chinese) study platform designed for the **DBFP2423: Java Programming** course. Built with a modern Macaron Glassmorphism design system, smooth keyframe animations, and zero-dependency client-side interactivity.

---

## 🎨 Premium Visual Identity

The hub features a curated **Macaron Aesthetic** designed for maximum engagement and visual relief during study sessions:
- **Dreamy Pastel Gradients:** Continuously animated background shifting between Rose Pink, Lavender, Soft Blue, and Mint Green.
- **Floating Radial Aura Blurs:** Large, translucent glowing backdrops drifting dynamically in the viewport.
- **Glassmorphism Containers:** Frosted glass cards (`backdrop-filter: blur(40px)`) with clean, high-contrast borders and charcoal-ink typography for optimal readability.

---

## 🚀 Key Features

### 1. 📅 Comprehensive Weekly Modules (Weeks 1–14)
Step-by-step guides covering the entire course syllabus:
- **Week 1-3:** Fundamentals of Computer Systems, Problem Solving, and Algorithm Design (Pseudocode/Flowcharts/NS-Diagrams).
- **Week 4-7:** Java Environment (JDK/JVM/javac), Variables & Primitive Types, Operators & Expressions, and I/O (Scanner/printf).
- **Week 8-10:** Selection Structures (`if-else`, `switch`) and Loops (`while`, `for`, nesting).
- **Week 11-12:** Methods (parameters, void vs. return types) and Library functions (`Math` class).
- **Week 13-14:** Java Revision and Group Project Demo reviews.

### 2. 🎮 Interactive Self-Assessments
Every module features a fully functional client-side practice suite:
- **Knowledge Check (Quiz):** 5 multiple-choice questions per week with instant correctness feedback.
- **Fill in the Blanks:** Inline code completions that turn green for correct syntax and red for errors.
- **Coding Practice:** 3 interactive tasks per week with "Show Answer" toggleable code editors.
- **Matching Game:** Interactive terms and definitions card-matching game.

### 3. 🌐 Dual-Language Translation Toggle
A unified, zero-dependency **CSS Class-Driven Translation Engine** allows students to instantly switch the entire interface between **English** and **Chinese** (`🌐 EN / 中文`) with a single click.

### 4. 📊 Concept Visualizations
Standard vector-native SVG flow diagrams illustrating compile pipelines, logic control flows, and hardware-software architectures.

---

## 📂 Project Structure

```bash
DBFP2423/
├── index.html            # Main Portal Dashboard (Week 1-14 navigator)
├── Java-Note.html        # Comprehensive Single-Page Application Note Hub
├── week1.html            # Week 1 Module
├── week2.html            # Week 2 Module
│   ...
├── week14.html           # Week 14 Module
├── assets/
│   └── macaron_java.png  # Premium Agnes AI generated 3D Java theme header graphic
└── walkthrough.md        # Technical changes walkthrough report
```

---

## 🛠️ How to Run Locally

Since the platform is built purely with **Vanilla HTML5, CSS3, and JavaScript**, no installation or server configuration is required:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/dbfp2423-java-hub.git
   cd dbfp2423-java-hub
   ```
2. **Open in Browser:**
   Simply double-click `index.html` to launch the study hub dashboard in any modern web browser.
3. **Optional (Local Dev Server):**
   If you have VS Code, right-click `index.html` and select **Open with Live Server**, or run:
   ```bash
   python -m http.server 8000
   ```

---

## 💻 Tech Stack & Design Architecture

- **Structural Layer:** Semantic HTML5 elements with accessibility elements.
- **Presentation Layer:** Hardware-accelerated CSS keyframe animations, customized CSS Variables, and responsive layouts (CSS Grid & Flexbox).
- **Behavioral Layer:** Clean Vanilla JS for SPA view routing, interactive game state, score tracking, and language toggles.
- **Fonts:** Futuristic `Orbitron` (Headings), clean `Rajdhani` (Body), and `JetBrains Mono` (Code snippets).

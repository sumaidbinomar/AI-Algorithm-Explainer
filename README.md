# BSD 404 - Algorithms II Interactive Teaching Tool

<p align="center">
  <strong>An offline, single-file, interactive visualizer for three advanced algorithms</strong><br/>
  <em>Simplex Method • Strassen's Matrix Multiplication • Diffie-Hellman Key Exchange</em>
</p>

<p align="center">
  <img alt="Course" src="https://img.shields.io/badge/Course-BSD%20404-blue"/>
  <img alt="Tech" src="https://img.shields.io/badge/Tech-HTML%2FCSS%2FVanilla%20JS-success"/>
  <img alt="Mode" src="https://img.shields.io/badge/Mode-Offline%20Ready-orange"/>
  <img alt="Single File" src="https://img.shields.io/badge/Structure-Single%20index.html-purple"/>
</p>

---

## Table of Contents

- [Project Overview](#project-overview)
- [Course CLO Mapping](#course-clo-mapping)
- [Core Features](#core-features)
- [Part-by-Part Breakdown](#part-by-part-breakdown)
- [UI/UX Highlights](#uiux-highlights)
- [Tech Stack and Constraints](#tech-stack-and-constraints)
- [How to Run](#how-to-run)
- [How to Use the Tool](#how-to-use-the-tool)
- [Educational Design](#educational-design)
- [Project Structure](#project-structure)
- [Deployment (GitHub Pages)](#deployment-github-pages)
- [Submission Checklist](#submission-checklist)
- [Author](#author)

---

## Project Overview

This project is a complete interactive teaching application built for **BSD 404 - Algorithms II**. It is designed to teach advanced algorithms through **animated visualization**, **step-by-step execution**, **live pseudocode tracing**, and **plain-language explanations**.

The entire application is contained in a single `index.html` file and works by simply opening it in a browser. No installation, internet, libraries, or server setup is required.

### Why this project matters

Instead of only showing final answers, the tool reveals algorithm behavior at each internal state transition:

- How and why each step is selected
- What mathematical operation is performed
- Which pseudocode line is active
- How intermediate values evolve until completion

This turns the project from a basic demo into a true **learning companion**.

---

## Course CLO Mapping

| CLO | Topic Requirement | Implemented Part | Marks |
|-----|-------------------|------------------|-------|
| CLO-1 | Linear Programming / DP / Sorting Networks | **Part 1: Simplex Method** | 10 |
| CLO-2 | Fast Matrix Multiplication / Parallel / FFT | **Part 2: Strassen's Algorithm** | 10 |
| CLO-3 | Number-Theoretic Cryptographic Algorithms | **Part 3: Diffie-Hellman** | 10 |

Total: **30 marks** (10 per part).

---

## Core Features

### Global Features (all 3 parts)

- Tab-based navigation for switching algorithms
- Independent state machine per part (`idle`, `ready`, `playing`, `paused`, `done`)
- Playback controls in consistent order:
  - **Build Steps → Step → Play → Pause → Reset**
- Adjustable speed (`0.25x`, `0.5x`, `1x`, `2x`, `4x`)
- Live step counter and status badges
- SVG-based animations with legends
- Pseudocode panel with active-line highlighting and tooltips
- Live explanation panel using real current values
- Statistics cards for operation counters
- Scrollable history table with clickable steps
- Preset examples for quick demonstrations
- Input validation with inline error feedback
- Responsive layout (desktop split view, mobile stacked view)

---

## Part-by-Part Breakdown

## Part 1: LP - The Simplex Method (CLO-1)

### What is visualized

- Feasible region in 2D
- Constraint boundaries
- Vertex-to-vertex simplex path
- Current point and objective progression
- Tableau updates with highlighted pivot row/column/cell

### Supported instructional scenarios

- Basic feasible LP
- Unbounded LP case
- Infeasible LP case
- Degenerate pivot behavior (ratio ties)

### Learning tools in this part

- Variable selection rule toggle (Largest Coefficient / Bland's Rule)
- Live tableau and pivot mechanics
- Duality snapshot panel support
- Worked example with computed optimal vertex and objective value

---

## Part 2: Strassen's Fast Matrix Multiplication (CLO-2)

### What is visualized

- Matrix partitioning into quadrants
- Intermediate products `P1..P7`
- Recombination into result blocks `C11..C22`
- Recursion tree view
- Complexity chart panel

### Input and scenario support

- Matrix sizes: `2x2` and `4x4`
- Manual matrix editing
- Randomized matrix generation
- Identity-matrix quick setup
- Preset examples for trace walkthroughs

### Learning tools in this part

- Explicit comparison between multiplication reduction and addition overhead
- Step-by-step decomposition and recomposition
- Real-time counters:
  - Multiplications
  - Additions
  - Recursive calls

---

## Part 3: Diffie-Hellman Key Exchange (CLO-3)

### What is visualized

- Public parameter agreement (`p`, `g`)
- Alice/Bob private-to-public value generation
- Message exchange flow
- Shared secret convergence
- Square-and-multiply trace table
- Color-mixing panel for conceptual key agreement intuition

### Input and scenario support

- Customizable `p`, `g`, `a`, `b`
- Input validation workflow
- Three preset cryptographic examples

### Learning tools in this part

- Explains why both sides derive the same secret
- Emphasizes discrete logarithm hardness
- Tracks modular exponentiation operations in detail

---

## UI/UX Highlights

- Dark, modern educational interface using CSS variables
- Two-column teaching layout:
  - Left: controls + educational panels
  - Right: visualization + pseudocode + history
- Color semantics for algorithm states (active, success, warning, error)
- Smooth transitions for state changes and highlights
- Sticky headers and stable table readability for long traces

---

## Tech Stack and Constraints

### Stack

- **HTML5**
- **CSS3**
- **Vanilla JavaScript (ES6+)**
- **SVG** for all visual rendering

### Constraints satisfied

- No external JavaScript libraries
- No external CSS frameworks
- No build tool required
- No backend required
- Offline-capable and single-file executable

---

## How to Run

### Option 1: Open directly (recommended)

1. Download or clone this repository.
2. Open `index.html` in any modern browser.
3. Start interacting immediately.

### Option 2: VS Code Live Preview (optional)

1. Open project folder in VS Code.
2. Use any static preview extension or browser preview.
3. Load `index.html`.

---

## How to Use the Tool

For each algorithm tab:

1. Provide custom input **or** select a preset.
2. Click **Build Steps**.
3. Use:
   - **Step** for manual progression
   - **Play/Pause** for animated progression
   - **Reset** to return to first step
4. Follow learning panels while running:
   - Visualization
   - Pseudocode (active line)
   - Explanation box
   - Statistics
   - History

Tip: click a row in the History table to jump directly to that recorded step.

---

## Educational Design

This project is intentionally built as a structured mini-lesson system per algorithm.

Each part includes:

- **Algorithm Overview** (what, how, when)
- **Key Insight Box** (core conceptual takeaway)
- **Worked Example** (numerical walkthrough)
- **Live pseudocode mapping** (theory tied to execution)

This supports both classroom demonstration and self-paced revision.

---

## Project Structure

```text
Algorithm Midterm Project/
├─ index.html            # Full application (styles + scripts + UI)
├─ PROJECT_BLUEPRINT.md  # Requirement and architecture specification
└─ README.md             # Project documentation
```

---

## Deployment (GitHub Pages)

1. Push repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main` (or your default branch)
   - Folder: `/ (root)`
4. Save settings.
5. Wait for GitHub Pages to publish.

Your app will be hosted as a static site and will run exactly like local mode.

---

## Submission Checklist

- [x] Single-file implementation in `index.html`
- [x] Three algorithm parts mapped to CLO-1 / CLO-2 / CLO-3
- [x] Interactive controls and animation playback
- [x] Pseudocode + explanation synchronization
- [x] Statistics and history tracking
- [x] Educational content and worked examples
- [x] Responsive and offline-capable design

---

## Author

**Omar, Sumaid Bin**  
Student ID: **20220001454**  
Course: **BSD 404 - Algorithms II**  
Instructor: **Dr. Arash Kermani**

---

If you want, I can also generate:

- a portfolio-style README variant with hero image placeholders,
- a shorter recruiter-friendly version,
- and a polished GitHub project description + topic tags for better discoverability.

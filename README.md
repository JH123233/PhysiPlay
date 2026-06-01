# PhysiPlay 🪐 — Interactive Physics Playground & AI Solver

<p align="left">
  <strong>Translate to:</strong> 
  <a href="README.ko.md">🇰🇷 한국어 (Korean)</a>
</p>

> **Visualize and experience the laws of physics in real-time.**  
> PhysiPlay is an interactive web platform featuring 9 dynamic physics simulation engines and a multimodal Gemini-powered AI Solver that reads physics problem images, solves them step-by-step, and generates matching canvas animations instantly.

---

## 🎥 Demonstration
*(Place a demonstration GIF or a screenshot here)*
![PhysiPlay Main Screenshot](path/to/screenshot.png)

---

## ✨ Key Features

### 1. 9 Interactive Physics Simulators (HTML5 Canvases)
Visualize fundamental physical phenomena in real-time. Use interactive sliders and drag-and-drop elements to manipulate parameters and watch the simulation adapt instantly using high-precision numerical integration (e.g., RK4).
- **Mechanics:** Projectile Motion, Collisions (elastic/inelastic), Uniformly Accelerated Linear Motion, Simple Pendulum
- **Electromagnetics:** Real-time electric field lines and equipotential lines mapping
- **Thermodynamics:** 1D heat transfer and temperature diffusion using a dynamic colormap
- **Structural Mechanics:** Structural beam stress visualization (bending moments and deflection) based on load types
- **Waves & Astronomy:** Wave superposition (constructive/destructive interference & beats), Keplerian orbits with adjustable eccentricity

### 2. Gemini 2.5 Flash-Powered AI Solver & Physics Teacher
- **AI Image Problem Solver:** Upload a photo of any physics problem (from textbooks or exams), and the Gemini 2.5 Flash model delivers a thorough, step-by-step markdown solution with equations rendered beautifully via KaTeX.
- **Dynamic Parameter Extraction & Animation:** The AI extracts exact values (initial velocity, mass, angles, etc.) into structured JSON format. PhysiPlay then uses this data to **generate and play a customized canvas simulation** representing the problem scenario.
- **In-Context AI Chatbot:** A friendly "Physics Teacher" chatbot rests in the bottom-right corner, fully aware of your active simulator context to answer any conceptual questions in real-time.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5 Canvas, Vanilla JavaScript, Vanilla CSS, KaTeX (for mathematical formulas)
- **Backend:** Python (`http.server`, `urllib`), Google Gemini API (`gemini-2.5-flash`)

---

## 🚀 Quick Start (Local Run)

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/physidogam.git
cd physidogam

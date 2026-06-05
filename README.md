# PhysiPlay 🪐 — Interactive Physics Playground & AI Solver

<p align="left">
  <strong>Translate to:</strong> 
  <a href="README.ko.md">🇰🇷 한국어 (Korean)</a>
</p>

> **Visualize and experience the laws of physics in real-time.**  
> PhysiPlay is an interactive web platform featuring 15 dynamic physics simulation engines and a multimodal Gemini-powered AI Solver that reads physics problem images, solves them step-by-step, and generates matching canvas animations instantly (including multi-object combined scenarios).

---

## 🎥 Demonstration
*(Place a demonstration GIF or a screenshot here)*
![PhysiPlay Main Screenshot](path/to/screenshot.png)

---

## ✨ Key Features

### 1. 15 Interactive Physics Simulators (HTML5 Canvases)
Visualize fundamental physical phenomena in real-time. Use interactive sliders and drag-and-drop elements to manipulate parameters and watch the simulation adapt instantly using high-precision numerical integration (e.g., RK4).
- **Mechanics:** 
  - Projectile Motion (궤적 & 낙하지점 시뮬레이션)
  - Collisions (탄성/비탄성 충돌 시 운동량 & 에너지 변화)
  - Uniformly Accelerated Linear Motion (등가속도 직선 운동)
  - Simple Pendulum (감쇠 진동 및 RK4 수치 적분)
- **Waves & Acoustics:**
  - Wave Superposition (보강/상쇄 간섭 및 맥놀이 현상)
- **Electromagnetics:**
  - Electric Field Lines (점전하 배치에 따른 등전위선 & 전기장선 가시화)
  - Electromagnetic Induction (자석 이동에 따른 패러데이 유도 기전력 & 렌츠의 법칙)
- **Thermodynamics:**
  - Heat Transfer (시간에 따른 1차원 온도 확산 컬러맵 가시화)
  - Heat Engine Cycles (Carnot, Otto, Diesel 사이클 P-V/T-s 선도 및 피스톤 연동)
- **Optics:**
  - Geometric Optics (매질의 굴절률과 입사각 조절, 스넬의 법칙 & 전반사 레이트레이싱)
- **Modern Physics & Space:**
  - Photoelectric Effect (빛의 진동수/세기에 따른 광전자 방출 및 빛의 입자성 탐구)
  - Keplerian Orbits (이심률과 초기 속도에 따른 행성 궤도 및 면적 속도 일정 법칙)
- **Fluid & Vibration Mechanics:**
  - Fluid Dynamics (파이프 형상 조절에 따른 베르누이 압력 저하 & 벤투리 효과)
  - Mechanical Vibration (질량·감쇠·강성 및 조화 외력에 따른 고유 진동수 공진 & 과도 응답 분석)

### 2. Gemini 2.5 Flash-Powered AI Solver & Physics Teacher
- **AI Image Problem Solver:** Upload a photo of any physics problem (from textbooks or exams), and the Gemini 2.5 Flash model delivers a thorough, step-by-step markdown solution with equations rendered beautifully via KaTeX.
- **Dynamic Parameter Extraction & Animation:** The AI extracts exact values (initial velocity, mass, angles, etc.) into structured JSON format. PhysiPlay then uses this data to **generate and play a customized canvas simulation** representing the problem scenario.
- **Advanced "Combined" Multi-Object Support:** The AI solver supports complex problems involving multiple interacting objects. It maps them into a generalized 2D Cartesian coordinate system with sign conventions ($+x$ right, $-x$ left, $+y$ up, $-y$ down) and departure delays, rendering multiple objects simultaneously and locating their exact collision/intersection coordinates (`meetPoint`).
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
```

### 2. Set Up Your Gemini API Key (Required 🔑)
To enable the AI Solver and chatbot capabilities, you need a Google Gemini API key.
1. Create a file named `api_key.txt` in the project root directory.
2. Go to [Google AI Studio](https://aistudio.google.com/), generate your API key, paste it into the `api_key.txt` file, and save.
   *(Note: The file should contain nothing but the API key string, e.g., `AIzaSy...`)*

### 3. Start the Server
Run the local Python server from the project root:
```bash
python server.py
```
*On Windows, you can also double-click the `PhysiPlay_실행.bat` file in the root directory to run the server.*

### 4. Open in Browser
Open your web browser and navigate to:
> **http://localhost:7788**

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

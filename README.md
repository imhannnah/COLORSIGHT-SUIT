<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-2.3+-000000?style=for-the-badge&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/WCAG-2.1_Compliant-blue?style=for-the-badge" />
</p>

<h1 align="center">🎨 ColorSight Suite</h1>

<p align="center">
  <strong>See the world through every set of eyes.</strong><br>
  A comprehensive web-based Color Vision Deficiency (CVD) toolkit for designers, developers, clinicians, and researchers.
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-modules">Modules</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-project-structure">Project Structure</a> •
  <a href="#-color-vision-deficiency">About CVD</a> •
  <a href="#-license">License</a>
</p>

---

## ✨ Features

- 🔬 **Scientific Accuracy** — Uses clinically validated CVD simulation matrices (Brettel et al.) for Protanopia, Deuteranopia, Tritanopia, and Achromatopsia
- 🧪 **Adaptive Testing** — 13-plate Ishihara-style exam with an adaptive engine that adjusts difficulty based on real-time performance
- 📊 **WCAG 2.1 Compliance** — Automated contrast ratio checking against AA and AAA standards
- 📄 **PDF Reports** — Downloadable clinical-grade exam reports with per-question analysis
- 🎯 **Confusion Trap Detection** — Identifies if users fall for CVD-specific confusion symbols
- ⏱️ **Response Time Analysis** — Classifies answer speeds to detect potential mild CVD even on correct answers
- 🖥️ **Privacy First** — All processing runs server-side; no images or data are ever stored
- 📱 **Fully Responsive** — Works seamlessly on desktop, tablet, and mobile devices

---

## 🧩 Modules

### 1. 👁️ Color Blindness Simulator

Upload any image and instantly visualize how it appears under all four major CVD types. Supports drag-and-drop upload and side-by-side comparison.

| CVD Type | Description | Prevalence |
| --- | --- | --- |
| Protanopia | Red-blind (L-cone absent) | ~1.3% males |
| Deuteranopia | Green-blind (M-cone absent) | ~5.0% males |
| Tritanopia | Blue-blind (S-cone absent) | ~0.01% all |
| Achromatopsia | Total color blindness | ~0.003% all |

---

### 2. ⊚ Ishihara Plate Generator

Create custom Ishihara test plates with any symbol or number, targeted at specific CVD types. Uses CVD-matrix-validated color palettes to ensure clinical accuracy.

- **Formats:** Download as **SVG**, **PNG**, or **JPG**
- **Custom symbols:** Use any 1–2 character symbol
- **Target CVD type:** Generate plates that test for specific deficiencies
- **2,500 dots** per plate with collision-free spatial placement

---

### 3. 📋 Adaptive Vision Examination

A full 13-plate adaptive Ishihara-style screening exam with:

- **Control plate** — Validates the user can see basic high-contrast symbols
- **Phase 1 (Easy)** — One screening plate per CVD type
- **Phase 2 (Medium)** — Intermediate difficulty with CVD-matrix-validated palettes
- **Phase 3 (Hard + Confusion)** — Adaptive plates with confusion traps
- **Adaptive Engine** — Redirects hard plates from strong types to weak types based on performance
- **Response Time Analysis** — Fast/normal/slow classification per difficulty level
- **Weighted Scoring** — Easy (1.0x), Medium (1.5x), Hard (2.0x)
- **PDF Report** — Downloadable report with full question review and CVD risk breakdown

---

### 4. 🔍 Accessibility Audit

Upload a design or screenshot and get a comprehensive WCAG accessibility analysis:

- Edge-aware region segmentation
- WCAG AA/AAA contrast ratio checking
- Adjacent-contrast analysis
- Text-area detection
- CVD-specific color merge detection
- Fix suggestions with accessible alternatives
- Heatmap visualization
- PDF audit report

---

## 🛠️ Tech Stack

| Layer | Technology |
| --- | --- |
| **Backend** | Python 3.10+, Flask 2.3+ |
| **Image Processing** | Pillow (PIL), NumPy |
| **PDF Generation** | ReportLab |
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Templating** | Jinja2 |
| **Color Science** | Custom CVD matrices (Brettel et al.) |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/imhannnah/COLORSIGHT-SUIT.git
   cd COLORSIGHT-SUIT
   ```

2. **Create a virtual environment** (recommended)

   ```bash
   python -m venv venv

   # Windows
   venv\Scripts\activate

   # macOS / Linux
   source venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**

   ```bash
   python app.py
   ```

5. **Open in browser**

   Navigate to `http://localhost:5000`

---

## 📁 Project Structure

```
COLORSIGHT-SUIT/
├── app.py                  # Main Flask application (all 4 modules)
├── requirements.txt        # Python dependencies
├── index.html              # Root HTML file
├── DEVLOG.md               # Development log
│
├── templates/              # Jinja2 HTML templates
│   ├── base.html           # Base layout template
│   ├── index.html          # Homepage / Dashboard
│   ├── simulator.html      # Color Blindness Simulator
│   ├── generator.html      # Ishihara Plate Generator
│   ├── exam_start.html     # Exam landing page
│   ├── exam.html           # Exam question page
│   ├── exam_result.html    # Exam results dashboard
│   ├── detector.html       # Accessibility Audit page
│   ├── about.html          # About CVD page
│   └── 404.html            # Error page
│
└── static/
    └── css/
        └── styles.css      # Complete stylesheet
```

---

##  🧬 Color Vision Deficiency

Color Vision Deficiency (CVD) affects over **300 million people** worldwide — approximately **8% of males** and **0.5% of females**. It is not a disease, but a variation in visual perception caused by absent or altered cone photoreceptors in the retina.

### How ColorSight Suite Helps

| Use Case | Module |
| --- | --- |
| "How does my design look to colorblind users?" | **Simulator** |
| "I need test plates for my research" | **Generator** |
| "Do I have color blindness?" | **Exam** |
| "Does my UI pass WCAG standards?" | **Audit** |

### CVD-Safe Design Principles

- ❌ **Never** use color as the only information channel
- ✅ **Always** pair color with shape, pattern, text, or icon
- 🔵 Use **blue/orange** instead of red/green for critical states
- 📐 Maintain **luminance contrast** even when hue is lost
- 🧪 **Test with simulation** before shipping

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**HANNA**
- GitHub: [@imhannnah](https://github.com/imhannnah)

---

<p align="center">
  <em>Built with ❤️ for a more accessible world.</em>
</p>

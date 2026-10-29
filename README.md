# Smart Presence AI | Multimodal Attendance & Engagement Agent

**Smart Presence AI** is an end-to-end multimodal classroom attendance and cognitive engagement monitoring platform developed by **[Shivnandni Takhtani](https://github.com/Shivnandnitakhtani)**. It integrates computer vision posture tracking, privacy-preserving ambient audio signal processing, rule-based multimodal fusion, and an interactive instructor copilot dashboard.

---

## 6-Milestone Architecture Overview

1. **Milestone 1 — Dependency & Environment Stack (`requirements.txt` & `package.json`)**:
   - Curated open-source stack covering Computer Vision (`opencv-python`, `mediapipe`), Audio Processing (`librosa`, `webrtcvad`), Backend/Agent APIs (`fastapi`, `google-generativeai`), and Analytics (`numpy`, `pandas`).
2. **Milestone 2 — Vision Module (`modules/vision_module.py`)**:
   - Multi-frame participant detection, sustained presence verification for automated attendance marking, and occlusion-resilient posture/gaze scoring.
3. **Milestone 3 — Audio Module (`modules/audio_module.py`)**:
   - Privacy-preserving acoustic telemetry that measures classroom decibel energy (`dB`) and speech activity ratios without speech-to-text recording.
4. **Milestone 4 — Multimodal Reasoning Agent (`modules/multimodal_agent.py`)**:
   - Explainable rule-based fusion combining visual focus and ambient audio cues into unified engagement metrics and affect states.
5. **Milestone 5 — Analytics & Recommendation Engine (`modules/analytics_engine.py`)**:
   - Translates low-level signal telemetry into context-aware instructor interventions and ethical session-level analytics.
6. **Milestone 6 — End-to-End Validation & Interactive Dashboard (`modules/validate_pipeline.py` & `src/App.jsx`)**:
   - Automated pipeline validation suite paired with a real-time React + Tailwind CSS dashboard, simulated classroom canvas, WebRTC camera stream, Copilot chat, and CSV report exporter.

---

## Repository Structure

```text
smart-presence-ai/
├── index.html
├── package.json
├── requirements.txt
├── README.md
├── MILESTONE_SUBMISSION_GUIDE.md
├── .env.example
├── .gitignore
├── modules/
│   ├── __init__.py
│   ├── vision_module.py
│   ├── audio_module.py
│   ├── multimodal_agent.py
│   ├── analytics_engine.py
│   └── validate_pipeline.py
└── src/
    ├── App.jsx
    └── main.jsx
```

---

## Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/Shivnandnitakhtani/SMART-PRESENCE-AI.git
cd SMART-PRESENCE-AI
```

### 2. Run the Interactive Frontend Dashboard
```bash
npm install
npm run dev
```

### 3. Run the Python Multimodal Pipeline Validation (Optional)
```bash
pip install -r requirements.txt
python3 -m modules.validate_pipeline
```

---

## Author

**Shivnandni Takhtani**  
GitHub: [@Shivnandnitakhtani](https://github.com/Shivnandnitakhtani)

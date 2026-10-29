# Smart Presence AI — SkillWallet Milestone Submission Guide
**Author**: Shivnandni Takhtani (`@Shivnandnitakhtani`)  
**Project Name**: Smart Presence AI — Multimodal Attendance & Engagement Agent

Below are the customized, ready-to-submit descriptions, approaches, processes, and technical details for all **6 Milestones** shown in your SkillWallet portal.

---

## Milestone 1: Dependency Identification & Environment Setup (`requirements.txt`)

### Approach
To build **Smart Presence AI**, the initial phase focused on selecting a cohesive, reliable stack of open-source software libraries capable of handling real-time computer vision, privacy-preserving acoustic signal analysis, multimodal rule-based reasoning, and interactive web visualization. Preference was given to lightweight, well-maintained Python and JavaScript packages that guarantee cross-platform stability and clean modularity.

### Process
1. Decomposed the **Smart Presence AI** architecture into core functional layers: visual participant tracking, ambient audio energy extraction, multimodal fusion API, and attendance report generation.
2. Selected specialized packages for each domain:
   - **Vision Processing**: `opencv-python`, `mediapipe`, `Pillow`
   - **Audio Signal Analysis**: `librosa`, `soundfile`, `pydub`, `webrtcvad`
   - **Backend & Multimodal Agent API**: `fastapi`, `uvicorn`, `pydantic`, `google-generativeai`, `python-dotenv`
   - **Data Storage & Session Analytics**: `numpy`, `pandas`, `scipy`
3. Validated version compatibility across all packages under Python 3.10+ to prevent dependency conflicts.
4. Recorded exact pinned versions inside `requirements.txt` and frontend packages inside `package.json`.
5. Audited the dependency tree to strip out redundant packages and minimize installation footprint.

### Technical Details
The `requirements.txt` file organizes dependencies into four structured groups:
- **Computer Vision Libraries**: Power multi-frame face/participant detection, posture estimation, and sustained presence verification for automated check-ins.
- **Audio Processing Libraries**: Compute root-mean-square (RMS) decibel energy and voice activity ratios from classroom audio without performing invasive speech-to-text transcription.
- **Agent & API Libraries**: Expose multimodal telemetry endpoints and optional Gemini AI copilot reasoning.
- **Analytics & Reporting Libraries**: Aggregate time-series engagement metrics and export structured CSV attendance ledgers.

---

## Milestone 2: Vision Module Development (`modules/vision_module.py`)

### Objective
This milestone implements the **Smart Presence AI Vision Module**, which detects classroom participants from live camera feeds or simulated video streams, tracks each individual across consecutive frames, and verifies sustained presence to mark attendance automatically without manual roll calls.

The module is engineered to remain resilient across real-world classroom challenges including natural student movement, partial occlusions, varying seating angles, and shifting ambient lighting. Its structured visual telemetry (posture state, gaze alignment, and frame-level confidence) feeds directly into the downstream multimodal reasoning engine.

---

## Milestone 3: Audio Module Development (`modules/audio_module.py`)

### Description
This milestone builds the **Smart Presence AI Audio Module**, which complements visual tracking by capturing the acoustic dynamics of the classroom through signal processing. It evaluates ambient decibel levels (`dB`) and voice activity ratios to gauge class participation, discussion energy, and quiet slumps.

To uphold strict student privacy in educational settings, the module operates purely on acoustic energy envelopes and spectral features—without recording raw conversations or performing speech recognition. These non-verbal audio cues are subsequently fused with visual posture signals for holistic engagement estimation.

---

## Milestone 4: Multimodal Agent Implementation (`modules/multimodal_agent.py`)

### Description
This milestone delivers the core **Smart Presence AI Multimodal Agent**, acting as the central reasoning layer of the platform. Rather than evaluating camera frames or microphone levels in isolation, the agent fuses outputs from both the Vision Module and the Audio Module using **interpretable, rule-based reasoning** (weighted 70% visual attention and 30% acoustic interaction).

The primary objective of this milestone is to guarantee that every engagement score, affect classification (`Focused & Interactive`, `Mild Confusion`, or `Passive Slump`), and attention alert is grounded in **transparent, explainable, and context-aware logic** tailored for real classrooms.

---

## Milestone 5: Analytics and Recommendation Engine (`modules/analytics_engine.py`)

### Description
This milestone transforms raw multimodal engagement scores and classroom telemetry into **human-readable, context-aware recommendations** via the **Smart Presence AI Analytics & Recommendation Engine**. It serves two complementary purposes:
1. Providing instructors with real-time pedagogical nudges (e.g., launching a quick concept poll, pausing to clarify a derivation, or triggering a micro-break when focus drops below 60%).
2. Generating session-level analytics and downloadable CSV reports that support student self-awareness and ethical classroom assessment.

---

## Milestone 6: System Validation, Pipeline Integration & Visualization (`modules/validate_pipeline.py` & `src/App.jsx`)

### Description
This final milestone validates the end-to-end reliability, responsiveness, and integration of **Smart Presence AI — Multimodal Attendance & Engagement Agent**. Automated verification tests confirm that the Vision Module, Audio Module, Multimodal Reasoning Agent, and Recommendation Engine operate accurately both as standalone components and within the unified pipeline.

Additionally, it provides an interactive **React + Tailwind CSS Instructor Dashboard** featuring a simulated classroom canvas, live WebRTC webcam mode, real-time telemetry gauges, an AI Instructor Copilot chat, and one-click CSV attendance export.

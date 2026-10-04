# EmotionSense – Text Emotion Analysis
### Text & Speech Analysis — Experiment 08: Emotion Analysis

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**EmotionSense** is a modern, standalone web application developed for the college **Text and Speech Analysis** curriculum. It demonstrates rule-based emotion detection from written text and vocal input using client-side Natural Language Processing (NLP) techniques and the Web Speech API.

---

## 🎯 Objective

Analyze text and identify the emotional state expressed by the user across six primary emotional categories:
- 😊 **Happy**
- 😢 **Sad**
- 😡 **Angry**
- 😨 **Fear**
- 😲 **Surprise**
- 😐 **Neutral**

> *“Emotion analysis attempts to identify the emotional state expressed in text or speech.”*  
> **Notice:** This is an **educational rule-based demonstration** designed to illuminate tokenization, morphological stemming, lexical dictionary matching, and modifier weighting.

---

## 🚀 Key Features

1. **Rule-Based Emotion Detection**:
   - Comprehensive emotion lexicons for all 6 target emotions.
   - Stem-based pattern matching (e.g., `happi*`, `excit*`, `crying`).
   - 2-word lookback window for linguistic **intensifiers** (*extremely*, *very*, *totally*) and **negations** (*not*, *never*, *no*).
   - High-arousal punctuation detection (exclamations `!`).

2. **Speech-to-Text Integration (🎤 Speak Emotion)**:
   - Uses browser-native Web Speech API (`webkitSpeechRecognition` / `SpeechRecognition`) to convert spoken voice directly into text for immediate emotional analysis.
   - Real-time audio waveform visualizer and status feedback.

3. **Emotion Distribution Chart & Confidence Score**:
   - Visual distribution meter rendering percentages across all six emotions summing to 100%.
   - Dynamic confidence metric calculation (e.g., *87%* for *“I am extremely happy with my project!”*).

4. **Token Highlighting & Keyword Evidence**:
   - Color-coded in-situ token highlighting showing which words influenced the classified emotional state.

5. **100% Client-Side**:
   - Zero external backend, zero server calls, zero API keys required.
   - Works fully offline on modern web browsers.

6. **Rich Interactive UI**:
   - Glassmorphic modern aesthetic with dark mode and light mode toggle.
   - Interactive Lexicon Dictionary explorer.
   - Preset selector for instant testing of all emotions.
   - Text-to-speech audio readout of classification results.

---

## 🧠 Algorithmic Pipeline

```
[ User Speech / Text Input ]
             │
             ▼
[ Tokenization & Stemming ]
(Split words, remove punctuation, extract stems)
             │
             ▼
[ Context & Modifier Lookback Window ]
(Detect intensifiers e.g. "extremely" x2.0, negations e.g. "not happy")
             │
             ▼
[ Multi-Lexicon Emotion Scoring ]
(Happy, Sad, Angry, Fear, Surprise, Neutral)
             │
             ▼
[ Distribution Normalization & Confidence ]
(Normalized 100% chart bars & calibrated confidence score)
             │
             ▼
[ Dashboard Presentation ]
(Hero card, emoji, confidence gauge, distribution bars, token highlight)
```

---

## 📂 Project Structure

```
TSA8/
├── index.html        # Main semantic HTML5 structure & UI layout
├── style.css         # Responsive styling, design tokens & animations
├── script.js         # Lexicon dictionary, NLP rules & speech engine
└── README.md         # Experiment documentation & academic guide
```

---

## 💻 How to Run Locally

Because this project is built entirely on vanilla HTML, CSS, and JavaScript, no build step or package manager is required:

1. Clone or download the repository:
   ```bash
   git clone https://github.com/kameshpa7-hash/TSA8.git
   cd TSA8
   ```

2. Open `index.html` directly in any modern browser (e.g., Google Chrome, Microsoft Edge, Mozilla Firefox):
   - Double-click `index.html`, OR
   - Run a local static server:
     ```bash
     npx serve .
     ```
     or
     ```bash
     python -m http.server 8000
     ```

3. Enter a sentence such as:
   > *“I am extremely happy with my project!”*  
   or click **🎤 Speak Emotion** to dictate with your microphone.

---

## 🔬 Sample Inputs & Results

| Input Statement | Dominant Emotion | Confidence | Key Factors Detected |
|---|---|---|---|
| *"I am extremely happy with my project!"* | 😊 **Happy** | **87%** | `happy` keyword + `extremely` intensifier (2.0x) |
| *"I feel so lonely and disappointed with the results."* | 😢 **Sad** | **84%** | `lonely`, `disappointed` |
| *"This terrible service makes me so furious and annoyed!"* | 😡 **Angry** | **88%** | `terrible`, `furious`, `annoyed` |
| *"I'm scared and terrified of the upcoming danger."* | 😨 **Fear** | **86%** | `scared`, `terrified`, `danger` |
| *"Wow! That was completely unexpected and amazing!"* | 😲 **Surprise** | **89%** | `wow`, `unexpected`, `amazing`, `!` |
| *"The meeting will take place at 3 PM in the conference room."* | 😐 **Neutral** | **85%** | Objective / factual vocabulary |

---

## 📜 Academic Reference

- **Course:** Text & Speech Analysis (TSA)
- **Experiment:** Experiment 08 — Emotion Analysis
- **Domain:** Natural Language Processing (NLP) & Speech Processing

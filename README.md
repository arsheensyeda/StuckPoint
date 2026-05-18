# StuckPoint — AI That Catches the Moment a Student Gives Up

> *"Not tracking grades. Tracking the exact moment before the grade is decided."*

[![Built for Hackathon](https://img.shields.io/badge/Built%20for-Hackathon-blueviolet)](.)
[![Track](https://img.shields.io/badge/Track-Skill%20Tank%20%7C%20Saasum%20AI-green)](.)
[![Single File](https://img.shields.io/badge/Stack-Single%20HTML%20file-orange)](.)
[![API](https://img.shields.io/badge/AI-Google%20Gemini%201.5%20Flash-blue)](.)

---

## 🧠 The Problem

Every day, students sit down to study alone — and quietly give up on problems they almost understood. A student reads a problem, stares at it for four minutes, starts writing, erases it, opens YouTube, and doesn't come back.

Nobody saw that moment. No teacher, no app, no platform.

Current edtech tools measure outcomes — scores, completion rates, streaks. **None of them watch what's happening inside a study session, in real time, at the level of a single problem.**

StuckPoint lives in that gap.

---

## 💡 What It Does

StuckPoint watches **how a student behaves** on a problem — not what they submit — and intervenes at the exact moment they're about to disengage.

### Behavioral signals tracked (client-side, no camera needed):
| Signal | What it means |
|---|---|
| ⏱ Time on problem | How long since last progress |
| ⌫ Backspace bursts | Going in circles, erasing repeatedly |
| — Idle streak | Cursor stopped — the "staring at the wall" signal |
| ⇥ Tab switches | The classic escape behavior |

These combine into a **real-time struggle score (0–100)**. When thresholds are crossed, StuckPoint intervenes with one of three escalating hints:

- **Level 1** — A warm nudge to get thinking
- **Level 2** — The core concept or formula they need
- **Level 3** — A simpler version of the problem to build the method

The student can dismiss any hint. StuckPoint never forces help.

---

## ✨ Features

### 🎓 Student View
- **3 subjects** — Physics, Chemistry, Maths (6 problems each, difficulty-tagged)
- **Live behavior tracker** — idle time, backspaces, tab switches, struggle score bar
- **3-level adaptive hints** — AI-generated via Gemini, with hand-written fallbacks (works offline)
- **Adaptive mode** — if you struggle on the same topic twice, easier prerequisite questions are auto-inserted
- **Session summary** — problems solved, hints used, time taken, personalised insight
- **Hint history** — collapsible panel showing all hints received this session
- **Message teacher** — direct chat widget in the sidebar

### 📄 Worksheet Generator
- Upload your own PDF, image, or paste notes
- PDF text extraction (PDF.js) + OCR for images (Tesseract.js)
- Auto topic detection via Gemini
- Generates entrance-exam style questions (Numerical / Conceptual / MCQ) from your material
- Generated questions plug directly into the same struggle-detection engine

### 🎯 Productivity Hub
- **Goal tracker** — set goals with targets, units, deadlines; track progress
- **Task board** — drag-and-drop Kanban (To Do / In Progress / Done)
- **Study timer** — Pomodoro / Deep Work / Custom; circular ring countdown; auto-logs study minutes on completion
- **Progress dashboard** — per-subject study time bars, 28-day study heatmap, streak counter
- **AI suggestions** — personalised tips based on your goals, weak topics, and study time

### 👩‍🏫 Teacher Dashboard
- **Live view** — all students' struggle scores updating every 3 seconds, color-coded by severity
- **Rankings** — leaderboard with 🥇🥈🥉, score = solved×100 − hints×10 − time/10
- **Student Goals** — see every student's goal progress in real time
- **Messaging** — chat with individual students directly from the dashboard

---

## 🛠 Tech Stack

| Layer | Tool |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript — zero dependencies |
| AI | Google Gemini 1.5 Flash (v1beta endpoint) |
| PDF extraction | PDF.js (CDN) |
| OCR | Tesseract.js (CDN) |
| Storage | localStorage (client-side) |
| Backend | None needed |

**Single file. No build step. No server. Open `index.html` in a browser and it works.**

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/stuckpoint.git
cd stuckpoint
```

### 2. Get a free Gemini API key
Go to **https://aistudio.google.com/apikey** — free, no credit card, 1500 requests/day.

### 3. Open the app
Just open `index.html` in your browser — Chrome or Firefox recommended.

### 4. Enter your API key
A golden banner will appear at the top. Paste your Gemini key and click **Save key**. It's stored in your browser's localStorage — you only need to do this once.

> **Note:** The app works without an API key — all hints fall back to hand-written, per-problem hints. The worksheet generator and AI suggestions require a key.

---

## 📁 File Structure

```
stuckpoint/
├── index.html     ← The entire application (HTML + CSS + JS)
└── README.md
```

---

## 🎯 Hackathon Tracks

**Primary: Skill Tank**
StuckPoint directly addresses the skill development gap — students who struggle alone without timely intervention fall behind. StuckPoint provides the real-time nudge that a good teacher would give.

**Also fits: Saasum AI**
The productivity hub (goals, tasks, timer, progress dashboard, AI suggestions) makes StuckPoint a complete AI-powered study companion, not just a hint tool.

---

## 🔒 Privacy

- No account required
- No data sent to any server except Gemini API calls (the problem text + hint request)
- All behavioral tracking is client-side only
- API key stored only in your browser's localStorage
- No camera, no keylogger, no personal data collected

---

## 👥 Team

Built at [Hackathon Name] · [Date]

| Name | Role |
|---|---|
| Arsheen | Idea, design, development |

---

## 📸 Screenshots

> *(Add screenshots here after recording)*

---

## 📜 License

MIT — free to use, modify, and build on.

---

*StuckPoint doesn't wait for failure. It intervenes in the 3-minute window that decides whether a student learns something — or gives up on it.*

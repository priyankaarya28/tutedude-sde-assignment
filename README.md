# tutedude-sde-assignment
# 🎥 Simple Video Proctoring System (Beginner-Friendly)

This is a **basic video proctoring system** built with **HTML, JavaScript, and Node.js**.  
It detects whether a candidate is focused during an online interview and flags unauthorized items (phones, books, extra devices).

---

## ✨ Features

### Frontend (index.html)
- Candidate **camera + microphone** recording.
- **Face detection** using `face-api.js`.
- **Focus detection**:
  - Logs if candidate looks away > 5s.
  - Logs if no face detected > 10s.
  - Flags if multiple faces detected.
- **Object detection** using `coco-ssd` (TensorFlow.js):
  - Detects phone, book, laptop, etc.
- **Event log with timestamps** (downloadable as JSON).
- **Video recording** (downloadable as `.webm`).
- Generates a **Proctoring Report** with Integrity Score.

### Backend (Optional)
- Built with **Node.js + Express + MongoDB**.
- Stores logs from frontend.
- API endpoint to fetch session report.

---

## 📦 Tech Stack

- **Frontend:** HTML, JavaScript, face-api.js, TensorFlow.js (coco-ssd)
- **Backend (optional):** Node.js, Express, MongoDB
- **Recording:** MediaRecorder API

---

## 🚀 How to Run

### 1. Frontend only (quick test)
1. Save `index.html` locally.
2. Open it in Chrome/Edge (modern browser).
3. Click **Start** → allow camera & microphone.
4. Events will be logged in real-time.
5. Click **Stop** → download video + logs, view report.

### 2. With Backend
1. Install dependencies:
   ```bash
   npm init -y
   npm install express body-parser mongodb

# 📱 WhatsApp Archive Chat Viewer

A smart, local-first utility designed to take your flat exported WhatsApp chat history (`.txt` logs inside a `.zip` file) and turn them into an interactive, visually beautiful conversation timeline. 

This project completely eliminates the need for external cloud databases by keeping your data private, safe, and stored directly in your local directory or personal cloud folder (like iCloud).

---

## 🚀 Project Vision & Tech Stack

This project is built as a decoupled, full-stack application structured into two clear modules:

### ⚙️ 1. The Core Engine (`backend-python`)
* **What it does:** Reads the raw chat export, automatically detects whether it came from an **iOS** or **Android** device, and uses Regular Expressions (`regex`) to parse timestamps, usernames, and media tags.
* **The Output:** It extracts messages and groups them into a structured `chat_history.json` file while neatly organizing photos and audio notes into a local `media/` folder.
* **Tech Stack:** Python, `re` (Regex), `zipfile`, and `json` modules. (Future update: **FastAPI** to handle real-time web uploads).

### 🎨 2. The User Interface (`frontend-react`) [Coming Soon]
* **What it does:** Reads the generated JSON data files and renders a fully interactive dashboard mimicking a real chat application.
* **Key Features:** A vertical contact sidebar navigation list, green and grey message speech bubbles, native image viewing, and inline audio playback for voice memos.
* **Tech Stack:** React, JavaScript (ES6+), Vite.

---

## 📂 Current Repository Structure

```text
whatsapp-archive-viewer/
│
├── 📂 backend-python/         <-- Active Python development directory
│   ├── main.py                <-- Core Regex parsing engine
│   └── ...
│
└── 📄 README.md              <-- This project overview guide
```

---

## 🛠️ How it works (The Workflow Plan)

1. **Export:** Export your desired chat from WhatsApp on your phone as a `.zip` file (including media).
2. **Parse:** Run the Python script over the file to break down text data into an organized JSON format.
3. **Organize:** The assets are automatically placed into a localized structure relative to your cloud storage.
4. **View:** Launch the React app locally to select and read through your fully reconstructed chat memories.


## 📂 Future Repository Structure

```text

whatsapp-archive-viewer/
│
├── 📂 backend-python/         <-- Move your current main.py and regex work here
│   ├── main.py
│   ├── requirements.txt      <-- Python dependencies (FastAPI, etc.)
│   └── ...
│
├── 📂 frontend-react/         <-- Create your React + Vite project here later
│   ├── src/
│   ├── public/
│   ├── package.json          <-- React dependencies
│   └── ...
│
└── 📄 README.md              <-- Explains the full-stack architecture

```


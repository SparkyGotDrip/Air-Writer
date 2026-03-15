# ✏️ Air Writer

Draw in the air with hand gestures using your webcam.

---

## 📦 Files

| File | Description |
|------|-------------|
| `air_writer_tkinter.py` | Desktop app with Tkinter UI |
| `air_writer_webapp/app.py` | Web app (Flask + WebSocket) |
| `air_writer_webapp/requirements.txt` | Python dependencies |
| `air_writer_webapp/render.yaml` | Deploy config for Render.com |

---

## 🖥️ Tkinter App (Desktop)

### Install
```bash
pip install opencv-python mediapipe numpy Pillow
```

### Run
```bash
python air_writer_tkinter.py
```

### Features
- Dark sidebar UI with color picker, brush slider, mode toggles
- Click buttons OR use hand gestures — both work simultaneously
- 8 colors, adjustable brush size, mirror + particle modes

---

## 🌐 Web App

### Install
```bash
cd air_writer_webapp
pip install -r requirements.txt
```

### Run locally
```bash
python app.py
# Open http://localhost:5000
```

### ⚠️ Important: The web app requires a physical webcam on the SERVER machine.
> If you run it on a cloud server (Render, Railway), the server won't have a webcam.
> The best free hosting options are explained below.

---

## 🚀 Free Hosting Options

### Option A — Run locally + expose with ngrok (Recommended!)
Best if you want to share your running webcam with others:
```bash
# 1. Start the web app
python app.py

# 2. In another terminal, install and run ngrok
pip install ngrok
ngrok http 5000

# 3. Share the ngrok URL — anyone can access your Air Writer!
```
ngrok free tier: https://ngrok.com

### Option B — Render.com (server needs webcam — use for UI only)
Render works if you have a webcam attached to the server, or you adapt
the app to accept webcam frames from the browser instead.

```bash
# 1. Push to GitHub
git init && git add . && git commit -m "Air Writer"
gh repo create air-writer --public --push

# 2. Go to https://render.com
# 3. New → Web Service → connect your repo
# 4. Build command: pip install -r requirements.txt
# 5. Start command: python app.py
# Free tier: 750 hrs/month
```

### Option C — Railway.app
Similar to Render, free $5 credit monthly:
```bash
# Install Railway CLI
npm install -g @railway/cli
railway login
railway init
railway up
```

### Option D — Replit (easiest for sharing)
1. Go to https://replit.com
2. New Repl → Import from GitHub
3. Add your files, click Run
4. Share the Replit URL

---

## 🤚 Gesture Reference

| Gesture | Action |
|---------|--------|
| ☝️ Index finger | Draw |
| ✌️ Two fingers | Erase |
| 🤟 Pinky only | Cycle color |
| 🖐️ Open palm | Clear canvas |
| 🤘 Three fingers (hold 1s) | Toggle particles |
| 🖖 Four fingers (hold 1s) | Toggle mirror mode |
| ✊ Fist | Idle / pause |

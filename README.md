# ✏️ Air Writer

Draw in the air with hand gestures using your webcam.

---

## 📦 Files

| File | Description |
|------|-------------|
| `air_writer_tkinter.py` | Desktop app with Tkinter UI |
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

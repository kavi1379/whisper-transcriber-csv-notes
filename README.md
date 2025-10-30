# 🎙️ FlagRecorder — Cross-Platform Smart Audio + Slide Recorder

**FlagRecorder** is a two-part recording and transcription system built for researchers and students.  
It combines an **Android recording app** and a **Windows transcription tool** to automatically capture, mark, and transcribe lectures or meetings slide-by-slide.

---

## 🔗 Overview

| Platform | Role | Technology |
|-----------|------|------------|
| **Android App** | Records high-quality audio, adds slide markers (Flag1, Flag2…) | Kotlin / Android SDK |
| **Windows Tool** | Transcribes audio (via Whisper AI) and aligns text to slide markers | Python + PyQt + Faster-Whisper |

Together, they form a seamless workflow for **lecture recording → slide-aligned transcription → bilingual note generation**.

---

## 🧩 Architecture


---

## 📱 Android App — Recorder & Marker

### 🎯 Main Features
- Foreground recording service with persistent notification controls  
- Automatic project folder creation in `Music/FlagRecorder/<ProjectName>`  
- Real-time broadcast updates (`rec.tick`) every 500 ms  
- Pausable and resumable via both UI and notification actions  
- Compatible with Android 6 → 14  
- Safe `registerReceiver()` logic for Android 13+

### 🧠 Key Components
| File | Description |
|------|--------------|
| `RecorderService.kt` | Core recording logic + ticker coroutine |
| `NotificationHelper.kt` | Builds playback control notifications |
| `MainActivity.kt` | Simple UI (timer, project name, buttons) |
| `Utils.kt` | Safe receiver registration wrappers |

### 🗂 Output Example

---

## 💻 Windows Tool — Whisper-Based Transcriber

### 🎧 Features
- Uses **OpenAI Whisper / Faster-Whisper** for accurate multilingual transcription  
- Automatically splits transcript into slide-based text blocks using CSV markers  
- Supports real-time or offline transcription  
- Exports `.csv`, `.txt`, and bilingual `.docx` outputs  
- GPU acceleration (CUDA support)

### ⚙️ Requirements
- Python ≥ 3.9  
- CUDA 11.8+ (for GPU models)  
- FFmpeg installed in PATH  

### 🔧 Install
```bash
pip install faster-whisper pandas PyQt6


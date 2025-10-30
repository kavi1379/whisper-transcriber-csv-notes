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


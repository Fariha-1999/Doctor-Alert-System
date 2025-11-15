# Doctor Alert System

A **Patient Voice-to-Text and Risk Alert System** using synthetic audio, transcription, BioBERT-based risk profiling, and automated email alerts. This system transcribes patient voice inputs, evaluates medical risk, stores data in a database, and notifies doctors when medium or high-risk conditions are detected.

---

## Project Overview

**Objective:**  
Convert patient speech into text, analyze medical risk levels, and alert doctors automatically for critical cases.

**Key Features:**
- Synthetic patient audio generation using gTTS.
- Audio preprocessing and transcription with OpenAI Whisper.
- Hybrid risk profiling using:
  - Keyword-based detection (high & medium risk terms)
  - Fine-tuned BioBERT classifier
- Automated email alerts for Medium/High-risk patients.
- Database storage (SQLite) of transcripts, risk profiling, and alerts.
- Evaluation metrics: WER, Precision, Recall, F1-score, alert reliability, and latency.

---

## Architecture & Technology Stack

**Frontend / Input:**  
- Text/voice input (synthetic or recorded patient audio)

**Processing Pipeline:**  
1. Audio preprocessing (Pydub)
2. Transcription (OpenAI Whisper)
3. Risk profiling (keywords + fine-tuned BioBERT)
4. Alert system (Gmail SMTP)

**Database & Storage:**  
- SQLite (`doctor_alert.db`) storing transcripts and alerts.

**Libraries & Frameworks:**  
- Python 3.10+  
- gTTS, Pydub, Whisper, Transformers, Torch, scikit-learn, pandas, fuzzywuzzy, jiwer  

---

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/DoctorAlertSystem.git
   cd DoctorAlertSystem

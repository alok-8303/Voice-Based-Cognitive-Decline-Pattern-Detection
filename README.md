# 🧠 MemoTag: Voice-Based Cognitive Decline Detection

A proof-of-concept pipeline for detecting early cognitive stress or impairment using speech features and unsupervised learning.

---

## 🎯 Objective

To analyze anonymized voice samples and extract early indicators of cognitive decline through a combination of audio signal processing and unsupervised machine learning techniques.

---

## 🔍 Methodology

### 1. Audio Preprocessing & Transcription
- Converted raw `.wav` files into text using OpenAI’s Whisper model.
- Cleaned and segmented transcripts for further analysis.

### 2. Feature Extraction
Extracted cognitive-linguistic features from both audio and transcript:
- **Speech Rate** (words per second)
- **Pauses** (via silence detection)
- **Hesitations** (e.g., "uh", "um")
- **Pitch Mean** and **Pitch Variability**

### 3. Anomaly Detection
- Standardized features using `StandardScaler`.
- Applied **Isolation Forest** to detect anomalies (possible cognitive stress indicators).
- Flagged outlier voice samples for further investigation.

---

## 📈 Sample Output

```text
Filename: sample3.wav
Speech Rate: 2.82
Pauses: 0
Hesitations: 0
Pitch Mean: 1312.11
Pitch Std: 987.10
➡️ Flagged as anomaly


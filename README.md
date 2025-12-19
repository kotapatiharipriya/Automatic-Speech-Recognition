# 🎙️ Automatic Speech Recognition (ASR)

This repository contains two Google Colab notebooks that perform **Automatic Speech Recognition (ASR)** (speech-to-text) on uploaded audio files.

## ✅ What’s included

### 1) ASR using Hugging Face Transformers (Wav2Vec2)
- Uses `transformers.pipeline("automatic-speech-recognition")`
- Model: **facebook/wav2vec2-large-960h**
- Workflow:
  1. Upload an audio file in Colab
  2. Load audio with `soundfile`
  3. Convert to `float32` NumPy array
  4. Transcribe using the Hugging Face ASR pipeline
  5. Print transcription

Notebook: `ASR.ipynb`

---

### 2) Audio Preprocessing + ASR using Google SpeechRecognition
- Converts uploaded audio to WAV using `pydub`
- Preprocessing:
  - Normalization (`librosa.util.normalize`)
  - Noise reduction (`noisereduce`)
- Visualization:
  - Waveform plot
  - Spectrogram plot
- Transcription:
  - Uses `speech_recognition` with **Google Speech Recognition**
- Saves transcription to `recognized_text.txt` and downloads it from Colab

Notebook: `ASR1.ipynb`

---

## 📌 Requirements (Colab)
These notebooks were built for Google Colab. The notebooks install dependencies directly using `pip`.

### ASR.ipynb installs
- `transformers`
- `pydub`
- `soundfile`

### ASR1.ipynb installs
- `pydub`
- `librosa`
- `numpy`
- `matplotlib`
- `speechrecognition`
- `noisereduce`
- `soundfile`

---

## ▶️ How to Run (Google Colab)

1. Open a notebook in Colab:
   - `ASR.ipynb` (Wav2Vec2 / Hugging Face)
   - `ASR1.ipynb` (Noise reduction + Google SpeechRecognition)

2. Run all cells from top to bottom

3. Upload an audio file when prompted (Colab upload widget)

4. View:
   - Printed transcription output
   - In `ASR1.ipynb`, waveform + spectrogram
   - In `ASR1.ipynb`, download `recognized_text.txt`

---

## 🧪 Notes / Tips
- For best results, use **clear speech** and a **WAV** file if possible.
- If audio is noisy, try the preprocessing notebook (`ASR1.ipynb`) first.
- `ASR.ipynb` uses a pretrained model and may be slower on CPU-only runtime.

---

## 🚀 Future Improvements
- Add support for longer audio by chunking/streaming
- Compare Wav2Vec2 vs Whisper models
- Add Word Error Rate (WER) evaluation if ground-truth text is available
- Add language selection and multi-language support

---

## 👩‍💻 Author
**Haripriya Kotapati**  
GitHub: https://github.com/kotapatiharipriya

# Updated-Akan-TTS
Akan Text-To-Speach Demo Update

Interactive web demo for an **Asante Twi** Text-to-Speech model fine-tuned with **VoxCPM2 (LoRA)** on Akan speech data (`Professor/akan-speech-data`, CC BY 4.0).

## Architecture

1. **Frontend (GitHub Pages)**: `index.html` and `styles.css` provide an Akan orthography keypad (`ɛ`, `ɔ`, `ŋ`, `ɲ`), unseen evaluation sentences, audio playback, and WAV download.
2. **Inference Backend (FastAPI / Hugging Face Spaces or Google Colab Tunnel)**: Receives `POST /synthesize` JSON payloads (`{"text": "..."}`) and returns generated `audio/wav` speech from the fine-tuned checkpoint.

## Setup & Deployment

1. Deploy your FastAPI inference backend (for example on Hugging Face Spaces) and copy its `/synthesize` URL:
   ```
   https://your-space.hf.space/synthesize
   ```
2. Upload `index.html`, `styles.css`, and `README.md` to your `akan-tts-demo` GitHub repository.
3. Open **Settings → Pages**, select **Deploy from a branch** (`main` / `/(root)`), and click **Save**.
4. Visit `https://<your-username>.github.io/akan-tts-demo/`, enter your backend URL, and test with unseen Asante Twi sentences.

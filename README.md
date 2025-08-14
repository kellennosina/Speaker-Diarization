🎙️ Speaker Diarization — “Who Spoke When?”
📌 Overview

Speaker diarization is the process of partitioning an audio stream into homogeneous segments according to the speaker identity. In simple terms: it’s figuring out “who spoke when” in an audio file.

This project uses state-of-the-art speech processing techniques to automatically detect, segment, and label speakers in an audio recording.

The pipeline supports:

Noise reduction for cleaner audio processing.

Voice activity detection (VAD) to detect speech segments.

Speaker embedding extraction using pre-trained models.

Clustering to assign segments to speakers.

Timestamped diarization output in text and/or visualization format.

🚀 Features

🔊 Handles noisy environments with preprocessing.

🧠 Uses pre-trained models for robust speaker embeddings.

⏱️ Generates timestamps for each speaker segment.

📊 Optional visualization of speaker timelines.

📁 Supports multiple audio formats (.wav, .mp3, etc.).

🛠️ Tech Stack

Python (Core implementation)

PyTorch / TensorFlow (For deep learning models)

pyannote.audio or SpeechBrain (Diarization pipeline)

Librosa & Soundfile (Audio processing)

Scikit-learn (Clustering)

Matplotlib (Visualization)

📂 Project Structure
speaker-diarization/
│
├── data/                 # Sample audio files
├── notebooks/            # Jupyter notebooks for experiments
├── src/                  # Core code (VAD, embedding, clustering)
├── requirements.txt      # Dependencies
├── README.md             # Project documentation
└── output/               # Diarization results (timestamps, plots)

⚙️ Installation
# Clone the repo
git clone https://github.com/your-username/speaker-diarization.git
cd speaker-diarization

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # (Linux/Mac)
venv\Scripts\activate     # (Windows)

# Install dependencies
pip install -r requirements.txt

▶️ Usage
python src/diarize.py --input data/sample.wav --output output/result.txt


Example output:

[0.00s - 3.45s] Speaker 1
[3.45s - 7.10s] Speaker 2
[7.10s - 9.00s] Speaker 1

📊 Visualization Example
from src.visualize import plot_diarization
plot_diarization("output/result.txt")

📈 Future Improvements

Real-time streaming diarization.

Integration with speech-to-text for speaker-attributed transcription.

Support for multilingual audio.

📜 License

This project is licensed under the MIT License.
